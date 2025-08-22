<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ávilaor Defender</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: 'Arial', sans-serif;
            background: linear-gradient(to bottom, #1a1a2e, #16213e);
            color: #fff;
            height: 100vh;
            overflow: hidden;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }
        
        #game-container {
            position: relative;
            width: 800px;
            height: 500px;
            border: 3px solid #4cc9f0;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 0 20px rgba(76, 201, 240, 0.5);
        }
        
        #game-canvas {
            background: #0f1538;
        }
        
        #ui-container {
            position: absolute;
            top: 10px;
            left: 10px;
            z-index: 10;
        }
        
        #score, #health {
            font-size: 20px;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }
        
        #health-bar {
            width: 200px;
            height: 20px;
            background: #444;
            border-radius: 10px;
            overflow: hidden;
            margin-bottom: 10px;
        }
        
        #health-fill {
            height: 100%;
            background: linear-gradient(to right, #ff0080, #f72585);
            width: 100%;
            transition: width 0.3s;
        }
        
        #start-screen, #game-over {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            background: rgba(10, 15, 40, 0.9);
            z-index: 20;
        }
        
        #game-over {
            display: none;
        }
        
        h1 {
            font-size: 48px;
            color: #4cc9f0;
            margin-bottom: 20px;
            text-shadow: 0 0 10px rgba(76, 201, 240, 0.8);
        }
        
        button {
            background: linear-gradient(to right, #4361ee, #3a0ca3);
            color: white;
            border: none;
            padding: 15px 30px;
            font-size: 18px;
            border-radius: 30px;
            cursor: pointer;
            margin: 20px 0;
            transition: all 0.3s;
            box-shadow: 0 0 15px rgba(67, 97, 238, 0.5);
        }
        
        button:hover {
            transform: scale(1.05);
            box-shadow: 0 0 20px rgba(67, 97, 238, 0.8);
        }
        
        p {
            font-size: 18px;
            max-width: 600px;
            text-align: center;
            line-height: 1.5;
        }
        
        .controls {
            margin-top: 20px;
            background: rgba(255, 255, 255, 0.1);
            padding: 15px;
            border-radius: 10px;
            text-align: center;
        }
    </style>
</head>
<body>
    <div id="game-container">
        <canvas id="game-canvas" width="800" height="500"></canvas>
        
        <div id="ui-container">
            <div id="score">Score: 0</div>
            <div id="health">Health: 100%</div>
            <div id="health-bar">
                <div id="health-fill"></div>
            </div>
        </div>
        
        <div id="start-screen">
            <h1>ÁVILAOR DEFENDER</h1>
            <p>Defend your realm against the incoming enemies! Use your mouse to aim and click to fire powerful energy bolts.</p>
            <button id="start-button">START GAME</button>
            <div class="controls">
                <p>CONTROLS: Mouse to aim - Click to shoot</p>
                <p>Survive as long as possible and get the highest score!</p>
            </div>
        </div>
        
        <div id="game-over">
            <h1>GAME OVER</h1>
            <p>Your score: <span id="final-score">0</span></p>
            <button id="restart-button">PLAY AGAIN</button>
        </div>
    </div>

    <script>
        // Game variables
        let canvas, ctx;
        let player;
        let enemies = [];
        let projectiles = [];
        let particles = [];
        let score = 0;
        let health = 100;
        let gameRunning = false;
        let animationId;
        let enemySpawnRate = 1000; // ms
        let lastEnemySpawn = 0;
        
        // Initialize game
        function init() {
            canvas = document.getElementById('game-canvas');
            ctx = canvas.getContext('2d');
            
            // Create player
            player = {
                x: canvas.width / 2,
                y: canvas.height / 2,
                radius: 20,
                color: '#4cc9f0'
            };
            
            // Event listeners
            canvas.addEventListener('click', shoot);
            document.getElementById('start-button').addEventListener('click', startGame);
            document.getElementById('restart-button').addEventListener('click', restartGame);
            
            // Initial render
            draw();
        }
        
        // Start the game
        function startGame() {
            document.getElementById('start-screen').style.display = 'none';
            gameRunning = true;
            score = 0;
            health = 100;
            enemies = [];
            projectiles = [];
            particles = [];
            updateScore();
            updateHealth();
            
            // Start game loop
            gameLoop();
        }
        
        // Game over
        function gameOver() {
            gameRunning = false;
            document.getElementById('final-score').textContent = score;
            document.getElementById('game-over').style.display = 'flex';
            cancelAnimationFrame(animationId);
        }
        
        // Restart game
        function restartGame() {
            document.getElementById('game-over').style.display = 'none';
            startGame();
        }
        
        // Main game loop
        function gameLoop(timestamp) {
            if (!gameRunning) return;
            
            // Clear canvas
            ctx.fillStyle = 'rgba(15, 21, 56, 0.2)';
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            
            // Spawn enemies
            if (timestamp - lastEnemySpawn > enemySpawnRate) {
                spawnEnemy();
                lastEnemySpawn = timestamp;
                
                // Increase difficulty over time
                if (enemySpawnRate > 300) {
                    enemySpawnRate -= 10;
                }
            }
            
            // Update and draw player
            drawPlayer();
            
            // Update and draw projectiles
            updateProjectiles();
            
            // Update and draw enemies
            updateEnemies();
            
            // Update and draw particles
            updateParticles();
            
            // Continue animation
            animationId = requestAnimationFrame(gameLoop);
        }
        
        // Draw static elements (for initial screen)
        function draw() {
            // Clear canvas
            ctx.fillStyle = '#0f1538';
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            
            // Draw player
            drawPlayer();
            
            // Draw some decorative elements for the start screen
            for (let i = 0; i < 5; i++) {
                drawDecorations();
            }
        }
        
        // Draw player
        function drawPlayer() {
            ctx.beginPath();
            ctx.arc(player.x, player.y, player.radius, 0, Math.PI * 2);
            ctx.fillStyle = player.color;
            ctx.fill();
            
            // Draw glow effect
            ctx.beginPath();
            ctx.arc(player.x, player.y, player.radius * 1.5, 0, Math.PI * 2);
            const gradient = ctx.createRadialGradient(
                player.x, player.y, player.radius,
                player.x, player.y, player.radius * 1.5
            );
            gradient.addColorStop(0, 'rgba(76, 201, 240, 0.5)');
            gradient.addColorStop(1, 'rgba(76, 201, 240, 0)');
            ctx.fillStyle = gradient;
            ctx.fill();
        }
        
        // Draw decorative elements for start screen
        function drawDecorations() {
            const x = Math.random() * canvas.width;
            const y = Math.random() * canvas.height;
            const radius = Math.random() * 5 + 2;
            const color = `hsl(${Math.random() * 360}, 100%, 70%)`;
            
            ctx.beginPath();
            ctx.arc(x, y, radius, 0, Math.PI * 2);
            ctx.fillStyle = color;
            ctx.fill();
        }
        
        // Spawn enemy
        function spawnEnemy() {
            const radius = Math.random() * 20 + 10;
            
            let x, y;
            if (Math.random() < 0.5) {
                x = Math.random() < 0.5 ? 0 - radius : canvas.width + radius;
                y = Math.random() * canvas.height;
            } else {
                x = Math.random() * canvas.width;
                y = Math.random() < 0.5 ? 0 - radius : canvas.height + radius;
            }
            
            const color = `hsl(${Math.random() * 60}, 100%, 50%)`;
            
            const angle = Math.atan2(player.y - y, player.x - x);
            const velocity = {
                x: Math.cos(angle) * (Math.random() * 1.5 + 1),
                y: Math.sin(angle) * (Math.random() * 1.5 + 1)
            };
            
            enemies.push({
                x, y, radius, color, velocity
            });
        }
        
        // Update enemies
        function updateEnemies() {
            for (let i = enemies.length - 1; i >= 0; i--) {
                const enemy = enemies[i];
                
                // Update position
                enemy.x += enemy.velocity.x;
                enemy.y += enemy.velocity.y;
                
                // Draw enemy
                ctx.beginPath();
                ctx.arc(enemy.x, enemy.y, enemy.radius, 0, Math.PI * 2);
                ctx.fillStyle = enemy.color;
                ctx.fill();
                
                // Check collision with player
                const dist = Math.hypot(player.x - enemy.x, player.y - enemy.y);
                if (dist - enemy.radius - player.radius < 1) {
                    // Player hit
                    health -= 10;
                    updateHealth();
                    createParticles(enemy);
                    enemies.splice(i, 1);
                    
                    if (health <= 0) {
                        gameOver();
                    }
                }
            }
        }
        
        // Shoot projectile
        function shoot(event) {
            if (!gameRunning) return;
            
            const rect = canvas.getBoundingClientRect();
            const mouseX = event.clientX - rect.left;
            const mouseY = event.clientY - rect.top;
            
            const angle = Math.atan2(mouseY - player.y, mouseX - player.x);
            const velocity = {
                x: Math.cos(angle) * 5,
                y: Math.sin(angle) * 5
            };
            
            projectiles.push({
                x: player.x,
                y: player.y,
                radius: 5,
                color: '#f72585',
                velocity
            });
        }
        
        // Update projectiles
        function updateProjectiles() {
            for (let i = projectiles.length - 1; i >= 0; i--) {
                const projectile = projectiles[i];
                
                // Update position
                projectile.x += projectile.velocity.x;
                projectile.y += projectile.velocity.y;
                
                // Remove if out of bounds
                if (projectile.x + projectile.radius < 0 || 
                    projectile.x - projectile.radius > canvas.width ||
                    projectile.y + projectile.radius < 0 || 
                    projectile.y - projectile.radius > canvas.height) {
                    projectiles.splice(i, 1);
                    continue;
                }
                
                // Draw projectile
                ctx.beginPath();
                ctx.arc(projectile.x, projectile.y, projectile.radius, 0, Math.PI * 2);
                ctx.fillStyle = projectile.color;
                ctx.fill();
                
                // Check collision with enemies
                for (let j = enemies.length - 1; j >= 0; j--) {
                    const enemy = enemies[j];
                    const dist = Math.hypot(projectile.x - enemy.x, projectile.y - enemy.y);
                    
                    if (dist - enemy.radius - projectile.radius < 1) {
                        // Hit enemy
                        createParticles(enemy);
                        
                        // Increase score
                        score += Math.floor(100 - enemy.radius);
                        updateScore();
                        
                        // Remove enemy and projectile
                        enemies.splice(j, 1);
                        projectiles.splice(i, 1);
                        break;
                    }
                }
            }
        }
        
        // Create particles on enemy destruction
        function createParticles(enemy) {
            for (let i = 0; i < enemy.radius * 2; i++) {
                particles.push({
                    x: enemy.x,
                    y: enemy.y,
                    radius: Math.random() * 2 + 1,
                    color: enemy.color,
                    velocity: {
                        x: (Math.random() - 0.5) * 4,
                        y: (Math.random() - 0.5) * 4
                    },
                    alpha: 1,
                    fade: 0.02
                });
            }
        }
        
        // Update particles
        function updateParticles() {
            for (let i = particles.length - 1; i >= 0; i--) {
                const particle = particles[i];
                
                // Update position
                particle.x += particle.velocity.x;
                particle.y += particle.velocity.y;
                
                // Fade out
                particle.alpha -= particle.fade;
                
                // Draw particle
                ctx.save();
                ctx.globalAlpha = particle.alpha;
                ctx.beginPath();
                ctx.arc(particle.x, particle.y, particle.radius, 0, Math.PI * 2);
                ctx.fillStyle = particle.color;
                ctx.fill();
                ctx.restore();
                
                // Remove if faded out
                if (particle.alpha <= 0) {
                    particles.splice(i, 1);
                }
            }
        }
        
        // Update score display
        function updateScore() {
            document.getElementById('score').textContent = `Score: ${score}`;
        }
        
        // Update health display
        function updateHealth() {
            document.getElementById('health').textContent = `Health: ${health}%`;
            document.getElementById('health-fill').style.width = `${health}%`;
        }
        
        // Initialize game when page loads
        window.onload = init;
    </script>
</body>
</html>
