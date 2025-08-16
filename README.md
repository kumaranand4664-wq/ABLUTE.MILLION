
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ABLUTE_MILLION - Premium Image & Social Media Tools</title>
    <meta name="description" content="Free online image tools and social media utilities at ABLUTE_MILLION">
    <meta name="keywords" content="image tools, png converter, jpg converter, image resizer, qr code generator, youtube thumbnail downloader">
    
    <!-- Google AdSense -->6283374890158723"
    <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-YOUR_ADSENSE_ID" crossorigin="anonymous"></script>
    
    <!-- Font Awesome for icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    
    <!-- Animate.css -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css">
    
    <style>
        :root {
            --primary-color: #6e48aa;
            --secondary-color: #9d50bb;
            --accent-color: #ff7e5f;
            --light-color: #f9f9f9;
            --dark-color: #333;
            --text-color: #444;
            --text-light: #666;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }
        
        body {
            background-color: #f5f5f5;
            color: var(--text-color);
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        header {
            background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
            color: white;
            padding: 1.5rem 0;
            text-align: center;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
            position: relative;
            overflow: hidden;
        }
        
        header::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 70%);
            transform: rotate(30deg);
            animation: shine 8s infinite linear;
        }
        
        @keyframes shine {
            0% { transform: rotate(30deg) translate(-10%, -10%); }
            100% { transform: rotate(30deg) translate(10%, 10%); }
        }
        
        .logo {
            font-size: 2.8rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
            position: relative;
            display: inline-block;
            animation: fadeInDown 1s ease;
        }
        
        .logo span {
            color: var(--accent-color);
        }
        
        .tagline {
            font-size: 1.2rem;
            opacity: 0.9;
            position: relative;
            animation: fadeIn 1.5s ease;
        }
        
        nav {
            background-color: #fff;
            padding: 1.2rem;
            box-shadow: 0 2px 15px rgba(0, 0, 0, 0.08);
            position: sticky;
            top: 0;
            z-index: 100;
            animation: slideInDown 0.8s ease;
        }
        
        nav ul {
            display: flex;
            justify-content: center;
            list-style: none;
            gap: 1.5rem;
        }
        
        nav ul li a {
            text-decoration: none;
            color: var(--primary-color);
            font-weight: 600;
            padding: 0.6rem 1.2rem;
            border-radius: 30px;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        nav ul li a::before {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 3px;
            background-color: var(--accent-color);
            transition: width 0.3s ease;
        }
        
        nav ul li a:hover, nav ul li a.active {
            color: var(--primary-color);
        }
        
        nav ul li a:hover::before, nav ul li a.active::before {
            width: 100%;
        }
        
        .container {
            max-width: 1200px;
            margin: 3rem auto;
            padding: 0 1.5rem;
            animation: fadeIn 1s ease;
        }
        
        .ad-banner {
            background-color: #f0f0f0;
            padding: 1.2rem;
            text-align: center;
            margin: 2rem 0;
            border-radius: 8px;
            border: 1px dashed #ccc;
            animation: fadeInUp 0.8s ease;
        }
        
        .page-content {
            display: none;
            animation: fadeIn 0.8s ease;
        }
        
        .page-content.active {
            display: block;
        }
        
        .featured-section {
            background-color: white;
            border-radius: 12px;
            padding: 2.5rem;
            margin-bottom: 3rem;
            box-shadow: 0 5px 25px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .featured-section:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }
        
        .featured-section::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(90deg, var(--primary-color), var(--secondary-color), var(--accent-color));
        }
        
        .section-title {
            color: var(--primary-color);
            margin-bottom: 2rem;
            font-size: 2rem;
            font-weight: 600;
            position: relative;
            display: inline-block;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 0;
            width: 60px;
            height: 4px;
            background-color: var(--accent-color);
            border-radius: 2px;
        }
        
        .card-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .card {
            background-color: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            position: relative;
            transform-style: preserve-3d;
        }
        
        .card:hover {
            transform: translateY(-10px) scale(1.02);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.12);
        }
        
        .card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, rgba(110,72,170,0.1) 0%, rgba(157,80,187,0.1) 100%);
            opacity: 0;
            transition: opacity 0.3s ease;
        }
        
        .card:hover::before {
            opacity: 1;
        }
        
        .card-img {
            height: 200px;
            background-color: #f0f0f0;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #999;
            position: relative;
            overflow: hidden;
        }
        
        .card-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }
        
        .card:hover .card-img img {
            transform: scale(1.1);
        }
        
        .card-content {
            padding: 1.8rem;
            position: relative;
        }
        
        .card-title {
            font-size: 1.3rem;
            margin-bottom: 0.8rem;
            color: var(--dark-color);
            font-weight: 600;
        }
        
        .card-desc {
            color: var(--text-light);
            margin-bottom: 1.5rem;
            font-size: 0.95rem;
        }
        
        .btn {
            display: inline-block;
            background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
            color: white;
            padding: 0.8rem 1.5rem;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            position: relative;
            overflow: hidden;
            box-shadow: 0 4px 15px rgba(110, 72, 170, 0.3);
        }
        
        .btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.2), transparent);
            transition: 0.5s;
        }
        
        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(110, 72, 170, 0.4);
        }
        
        .btn:hover::before {
            left: 100%;
        }
        
        /* Tool Modal */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.8);
            z-index: 2000;
            overflow-y: auto;
            animation: fadeIn 0.3s ease;
        }
        
        .modal-content {
            background-color: white;
            margin: 3rem auto;
            padding: 2.5rem;
            border-radius: 12px;
            max-width: 900px;
            width: 90%;
            box-shadow: 0 10px 50px rgba(0,0,0,0.2);
            position: relative;
            transform: scale(0.9);
            opacity: 0;
            animation: modalOpen 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275) forwards;
        }
        
        @keyframes modalOpen {
            to { transform: scale(1); opacity: 1; }
        }
        
        .close-modal {
            position: absolute;
            top: 1.5rem;
            right: 1.5rem;
            font-size: 1.8rem;
            cursor: pointer;
            color: #999;
            transition: all 0.3s ease;
            width: 40px;
            height: 40px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
        }
        
        .close-modal:hover {
            color: var(--primary-color);
            background-color: #f0f0f0;
            transform: rotate(90deg);
        }
        
        /* Tool Interface */
        .tool-interface {
            display: flex;
            flex-direction: column;
            height: 500px;
        }
        
        .tool-header {
            background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
            color: white;
            padding: 1.2rem;
            text-align: center;
            font-weight: 600;
            margin-bottom: 1.5rem;
            border-radius: 8px 8px 0 0;
            font-size: 1.4rem;
            box-shadow: 0 4px 15px rgba(110, 72, 170, 0.3);
        }
        
        .tool-body {
            flex: 1;
            display: flex;
            flex-direction: column;
        }
        
        .tool-input {
            padding: 1.5rem;
            background-color: white;
            border: 1px solid #eee;
            border-radius: 8px;
            margin-bottom: 1.5rem;
            text-align: center;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
        }
        
        .file-upload {
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 2.5rem;
            border: 2px dashed #ccc;
            border-radius: 8px;
            margin-bottom: 1.5rem;
            transition: all 0.3s ease;
            cursor: pointer;
        }
        
        .file-upload:hover {
            border-color: var(--primary-color);
            background-color: rgba(110, 72, 170, 0.05);
        }
        
        .file-upload i {
            font-size: 3.5rem;
            color: var(--primary-color);
            margin-bottom: 1.5rem;
            transition: all 0.3s ease;
        }
        
        .file-upload:hover i {
            transform: scale(1.1);
            color: var(--secondary-color);
        }
        
        .file-upload p {
            color: var(--text-light);
            font-size: 1rem;
            margin-bottom: 1rem;
        }
        
        .file-upload input[type="file"] {
            display: none;
        }
        
        .tool-options {
            display: flex;
            gap: 1rem;
            margin-bottom: 1.5rem;
            flex-wrap: wrap;
            justify-content: center;
        }
        
        .tool-options label {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            background-color: #f5f5f5;
            padding: 0.8rem 1.2rem;
            border-radius: 30px;
            font-size: 0.9rem;
            transition: all 0.3s ease;
        }
        
        .tool-options label:hover {
            background-color: #e0e0e0;
        }
        
        .tool-result {
            flex: 1;
            padding: 1.5rem;
            background-color: #f9f9f9;
            border: 1px solid #eee;
            border-radius: 8px;
            overflow-y: auto;
            text-align: center;
            animation: fadeIn 0.5s ease;
        }
        
        .tool-result img {
            max-width: 100%;
            margin-top: 1.5rem;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
        }
        
        .tool-result img:hover {
            transform: scale(1.02);
            box-shadow: 0 8px 25px rgba(0,0,0,0.15);
        }
        
        /* Loading spinner */
        .spinner {
            display: inline-block;
            width: 24px;
            height: 24px;
            border: 3px solid rgba(110, 72, 170, 0.3);
            border-radius: 50%;
            border-top-color: var(--primary-color);
            animation: spin 1s ease-in-out infinite;
        }
        
        @keyframes spin {
            to { transform: rotate(360deg); }
        }
        
        /* Chatbot styles */
        #chatbot-container {
            position: fixed;
            bottom: 30px;
            right: 30px;
            width: 380px;
            z-index: 1000;
            box-shadow: 0 10px 30px rgba(0,0,0,0.15);
            border-radius: 15px;
            overflow: hidden;
            font-family: 'Poppins', sans-serif;
            transform: translateY(20px);
            opacity: 0;
            animation: fadeInUp 0.5s ease 1s forwards;
        }
        
        #chat-header {
            background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
            color: white;
            padding: 18px;
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 4px 15px rgba(110, 72, 170, 0.3);
        }
        
        #chat-toggle {
            font-size: 24px;
            font-weight: bold;
            transition: transform 0.3s ease;
        }
        
        #chat-body {
            height: 0;
            transition: height 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            background: white;
            overflow: hidden;
        }
        
        #chat-body.expanded {
            height: 450px;
            border-left: 1px solid #eee;
            border-right: 1px solid #eee;
        }
        
        #chat-messages {
            height: 340px;
            padding: 20px;
            overflow-y: auto;
            background: #f9f9f9;
        }
        
        .user-message {
            text-align: right;
            margin: 15px 0;
            animation: fadeInRight 0.4s ease;
        }
        
        .bot-message {
            text-align: left;
            margin: 15px 0;
            animation: fadeInLeft 0.4s ease;
        }
        
        .message-bubble {
            display: inline-block;
            max-width: 80%;
            padding: 12px 18px;
            border-radius: 20px;
            word-wrap: break-word;
            line-height: 1.5;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
        }
        
        .user-message .message-bubble {
            background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
            color: white;
            border-bottom-right-radius: 5px;
        }
        
        .bot-message .message-bubble {
            background: #fff;
            color: var(--text-color);
            border-bottom-left-radius: 5px;
            border: 1px solid #eee;
        }
        
        #chat-input-container {
            padding: 15px;
            background: white;
            border-top: 1px solid #eee;
            display: flex;
            align-items: center;
        }
        
        #user-input {
            flex: 1;
            padding: 12px 18px;
            border: 1px solid #ddd;
            border-radius: 30px;
            outline: none;
            font-family: 'Poppins', sans-serif;
            transition: all 0.3s ease;
        }
        
        #user-input:focus {
            border-color: var(--primary-color);
            box-shadow: 0 0 0 3px rgba(110, 72, 170, 0.2);
        }
        
        #send-btn {
            margin-left: 12px;
            padding: 12px 18px;
            background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
            color: white;
            border: none;
            border-radius: 30px;
            cursor: pointer;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 4px 15px rgba(110, 72, 170, 0.3);
        }
        
        #send-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(110, 72, 170, 0.4);
        }
        
        /* Typing indicator */
        .typing-indicator {
            display: flex;
            padding: 12px 18px;
            background: #fff;
            border-radius: 20px;
            width: fit-content;
            margin-bottom: 15px;
            border: 1px solid #eee;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
        }
        
        .typing-dot {
            width: 10px;
            height: 10px;
            background: var(--text-light);
            border-radius: 50%;
            margin: 0 3px;
            animation: typingAnimation 1.4s infinite ease-in-out;
        }
        
        .typing-dot:nth-child(1) {
            animation-delay: 0s;
        }
        
        .typing-dot:nth-child(2) {
            animation-delay: 0.2s;
        }
        
        .typing-dot:nth-child(3) {
            animation-delay: 0.4s;
        }
        
        @keyframes typingAnimation {
            0%, 60%, 100% { transform: translateY(0); }
            30% { transform: translateY(-5px); }
        }
        
        /* Social Links */
        .social-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin: 2rem 0;
        }
        
        .social-link {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
            color: white;
            font-size: 1.5rem;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(110, 72, 170, 0.3);
            position: relative;
            overflow: hidden;
        }
        
        .social-link::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.3), transparent);
            transition: 0.5s;
        }
        
        .social-link:hover {
            transform: translateY(-5px) rotate(5deg);
            box-shadow: 0 8px 25px rgba(110, 72, 170, 0.4);
        }
        
        .social-link:hover::before {
            left: 100%;
        }
        
        /* About Section */
        .about-section {
            background: linear-gradient(135deg, rgba(110,72,170,0.05) 0%, rgba(157,80,187,0.05) 100%);
            border-radius: 12px;
            padding: 3rem;
            margin: 3rem 0;
            text-align: center;
            border: 1px solid rgba(110,72,170,0.1);
        }
        
        .about-section h2 {
            color: var(--primary-color);
            margin-bottom: 1.5rem;
            font-size: 2rem;
        }
        
        .about-section p {
            color: var(--text-light);
            max-width: 800px;
            margin: 0 auto 2rem;
            line-height: 1.8;
        }
        
        .instagram-handle {
            display: inline-block;
            background: linear-gradient(45deg, #405DE6, #5851DB, #833AB4, #C13584, #E1306C, #FD1D1D);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            font-weight: 600;
            font-size: 1.2rem;
            margin-top: 1rem;
        }
        
        footer {
            background-color: var(--dark-color);
            color: white;
            text-align: center;
            padding: 3rem 0;
            margin-top: 4rem;
            position: relative;
        }
        
        footer::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(90deg, var(--primary-color), var(--secondary-color), var(--accent-color));
        }
        
        .footer-links {
            display: flex;
            justify-content: center;
            margin-bottom: 2rem;
            flex-wrap: wrap;
            gap: 1.5rem;
        }
        
        .footer-links a {
            color: #ccc;
            text-decoration: none;
            transition: all 0.3s ease;
            position: relative;
            padding: 0.5rem 0;
        }
        
        .footer-links a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--accent-color);
            transition: width 0.3s ease;
        }
        
        .footer-links a:hover {
            color: white;
        }
        
        .footer-links a:hover::after {
            width: 100%;
        }
        
        .copyright {
            opacity: 0.8;
            font-size: 0.9rem;
            margin-top: 1.5rem;
        }
        
        /* Scrollbar styling */
        ::-webkit-scrollbar {
            width: 8px;
        }
        
        ::-webkit-scrollbar-track {
            background: #f1f1f1;
            border-radius: 10px;
        }
        
        ::-webkit-scrollbar-thumb {
            background: linear-gradient(var(--primary-color), var(--secondary-color));
            border-radius: 10px;
        }
        
        ::-webkit-scrollbar-thumb:hover {
            background: var(--secondary-color);
        }
        
        @media (max-width: 992px) {
            .container {
                padding: 0 1.2rem;
            }
            
            .card-grid {
                grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            }
            
            .featured-section {
                padding: 2rem;
            }
        }
        
        @media (max-width: 768px) {
            nav ul {
                flex-direction: column;
                align-items: center;
                gap: 0.8rem;
            }
            
            nav ul li {
                width: 100%;
                text-align: center;
            }
            
            nav ul li a {
                display: block;
                width: 100%;
            }
            
            .card-grid {
                grid-template-columns: 1fr;
            }
            
            .modal-content {
                width: 95%;
                padding: 1.5rem;
            }
            
            #chatbot-container {
                width: 320px;
                right: 15px;
                bottom: 15px;
            }
            
            .featured-section {
                padding: 1.8rem;
            }
            
            .about-section {
                padding: 2rem 1.5rem;
            }
        }
        
        @media (max-width: 480px) {
            .logo {
                font-size: 2.2rem;
            }
            
            .tagline {
                font-size: 1rem;
            }
            
            .section-title {
                font-size: 1.6rem;
            }
            
            .btn {
                padding: 0.7rem 1.2rem;
                font-size: 0.9rem;
            }
            
            #chatbot-container {
                width: calc(100% - 30px);
                right: 15px;
            }
            
            .tool-options {
                flex-direction: column;
                align-items: flex-start;
            }
            
            .tool-options label {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="logo">ABLUTE<span>_MILLION</span></div>
        <div class="tagline">Premium Online Image & Social Media Tools</div>
    </header>
    
    <nav>
        <ul>
            <li><a href="#" class="nav-link active" data-page="image-tools">Image Tools</a></li>
            <li><a href="#" class="nav-link" data-page="social-tools">Social Media Tools</a></li>
        </ul>
    </nav>
    
    <div class="container">
        <!-- Top Ad Banner -->6283374890158723"
        <div class="ad-banner">
            <!-- Google AdSense Ad Unit -->6283374890158723"
            <ins class="adsbygoogle"
                 style="display:block"
                 data-ad-client="ca-pub-YOUR_ADSENSE_ID"
                 data-ad-slot="6283374890158723"
                 data-ad-format="auto"
                 data-full-width-responsive="true"></ins>
            <script>
                 (adsbygoogle = window.adsbygoogle || []).push({});
            </script>
        </div>
        
        <!-- Image Tools Page -->
        <div id="image-tools" class="page-content active">
            <div class="featured-section">
                <h2 class="section-title">Image Conversion Tools</h2>
                <div class="card-grid">
                    <div class="card">
                        <div class="card-img">
                            <img src="https://images.unsplash.com/photo-1633356122544-f134324a6cee?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=600&q=80" alt="PNG Converter">
                        </div>
                        <div class="card-content">
                            <h3 class="card-title">Image to PNG Converter</h3>
                            <p class="card-desc">Convert any image format to PNG while preserving transparency.</p>
                            <button class="btn try-tool" data-tool="png-converter">Convert Now</button>
                        </div>
                    </div>
                    <div class="card">
                        <div class="card-img">
                            <img src="https://images.unsplash.com/photo-1633356122102-3fe601e05bd2?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=600&q=80" alt="JPG Converter">
                        </div>
                        <div class="card-content">
                            <h3 class="card-title">Image to JPG Converter</h3>
                            <p class="card-desc">Convert images to JPG format with adjustable quality settings.</p>
                            <button class="btn try-tool" data-tool="jpg-converter">Convert Now</button>
                        </div>
                    </div>
                    <div class="card">
                        <div class="card-img">
                            <img src="https://images.unsplash.com/photo-1516035069371-29a1b244cc32?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=600&q=80" alt="Image Resizer">
                        </div>
                        <div class="card-content">
                            <h3 class="card-title">Image Resizer</h3>
                            <p class="card-desc">Resize your images to any dimensions while maintaining aspect ratio.</p>
                            <button class="btn try-tool" data-tool="image-resizer">Resize Now</button>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Middle Ad Banner -->6283374890158723"
            <div class="ad-banner">6283374890158723"
                <!-- Google AdSense Ad Unit -->6283374890158723"
                <ins class="adsbygoogle"
                     style="display:block"
                     data-ad-client="6283374890158723"
                     data-ad-slot="YOUR_AD_UNIT_ID_MIDDLE"6283374890158723"
                     data-ad-format="auto"
                     data-full-width-responsive="true"></ins>
                <script>
                     (adsbygoogle = window.adsbygoogle || []).push({});
                </script>
            </div>
            
            <div class="featured-section">
                <h2 class="section-title">Image Optimization Tools</h2>
                <div class="card-grid">
                    <div class="card">
                        <div class="card-img">
                            <img src="https://images.unsplash.com/photo-1558494949-ef010cbdcc31?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=600&q=80" alt="Image Compressor">
                        </div>
                        <div class="card-content">
                            <h3 class="card-title">Image Compressor</h3>
                            <p class="card-desc">Reduce image file size without noticeable quality loss.</p>
                            <button class="btn try-tool" data-tool="image-compressor">Compress Now</button>
                        </div>
                    </div>
                    <div class="card">
                        <div class="card-img">
                            <img src="https://images.unsplash.com/photo-1590845947676-fa2576f401d4?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=600&q=80" alt="Image Cropper">
                        </div>
                        <div class="card-content">
                            <h3 class="card-title">Image Cropper</h3>
                            <p class="card-desc">Crop images to remove unwanted areas or change aspect ratio.</p>
                            <button class="btn try-tool" data-tool="image-cropper">Crop Now</button>
                        </div>
                    </div>
                    <div class="card">
                        <div class="card-img">
                            <img src="https://images.unsplash.com/photo-1626785774573-4b799315345d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=600&q=80" alt="Base64 Converter">
                        </div>
                        <div class="card-content">
                            <h3 class="card-title">Image to Base64</h3>
                            <p class="card-desc">Convert images to Base64 string for web development.</p>
                            <button class="btn try-tool" data-tool="base64-converter">Convert Now</button>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="featured-section">
                <h2 class="section-title">Specialty Image Tools</h2>
                <div class="card-grid">
                    <div class="card">
                        <div class="card-img">
                            <img src="https://images.unsplash.com/photo-1633356122544-f134324a6cee?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=600&q=80" alt="WebP Converter">
                        </div>
                        <div class="card-content">
                            <h3 class="card-title">WebP to PNG</h3>
                            <p class="card-desc">Convert WebP images to PNG format for wider compatibility.</p>
                            <button class="btn try-tool" data-tool="webp-converter">Convert Now</button>
                        </div>
                    </div>
                    <div class="card">
                        <div class="card-img">
                            <img src="https://images.unsplash.com/photo-1633356122544-f134324a6cee?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=600&q=80" alt="GIF Maker">
                        </div>
                        <div class="card-content">
                            <h3 class="card-title">GIF Maker</h3>
                            <p class="card-desc">Create animated GIFs from images or videos.</p>
                            <button class="btn try-tool" data-tool="gif-maker">Create GIF</button>
                        </div>
                    </div>
                    <div class="card">
                        <div class="card-img">
                            <img src="https://images.unsplash.com/photo-1633356122544-f134324a6cee?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=600&q=80" alt="QR Code Generator">
                        </div>
                        <div class="card-content">
                            <h3 class="card-title">QR Code Generator</h3>
                            <p class="card-desc">Create custom QR codes for URLs, text, or contact information.</p>
                            <button class="btn try-tool" data-tool="qr-generator">Generate QR</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- Social Media Tools Page -->
        <div id="social-tools" class="page-content">
            <div class="featured-section">
                <h2 class="section-title">YouTube Tools</h2>
                <div class="card-grid">
                    <div class="card">
                        <div class="card-img">
                            <img src="https://images.unsplash.com/photo-1611162616475-46b635cb6868?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=600&q=80" alt="YouTube Thumbnail Downloader">
                        </div>
                        <div class="card-content">
                            <h3 class="card-title">YouTube Thumbnail Downloader</h3>
                            <p class="card-desc">Download high-quality thumbnails from any YouTube video.</p>
                            <button class="btn try-tool" data-tool="yt-thumbnail">Download Now</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- About Section -->
        <div class="about-section">
            <h2>About ABLUTE_MILLION</h2>
            <p>ABLUTE_MILLION provides premium online tools for image conversion, optimization, and social media needs. Our mission is to offer high-quality, easy-to-use tools that help creators and businesses enhance their digital content.</p>
            <p>Follow us on Instagram for updates and tips:</p>
            <div class="social-links">
                <a href="https://instagram.com/official__ankit__0005" class="social-link" target="_blank" title="Follow on Instagram">
                    <i class="fab fa-instagram"></i>
                </a>
            </div>
            <div class="instagram-handle">@official__ankit__0005</div>
        </div>
        
        <!-- Bottom Ad Banner -->
        <div class="ad-banner">
            <!-- Google AdSense Ad Unit -->6283374890158723"
            <ins class="adsbygoogle"
                 style="display:block"
                 data-ad-client="6283374890158723"
                 data-ad-slot="YOUR_AD_UNIT_ID_BOTTOM"6283374890158723"
                 data-ad-format="auto"
                 data-full-width-responsive="true"></ins>
            <script>
                 (adsbygoogle = window.adsbygoogle || []).push({});
            </script>
        </div>
    </div>
    
    <!-- Image Tools Modals -->
    <div id="png-converter-modal" class="modal">
        <div class="modal-content">
            <span class="close-modal">&times;</span>
            <div class="tool-interface">
                <div class="tool-header">Image to PNG Converter</div>
                <div class="tool-body">
                    <div class="tool-input">
                        <div class="file-upload">
                            <i class="fas fa-file-image"></i>
                            <p>Drag & drop your image here or click to browse</p>
                            <input type="file" id="png-file-input" accept="image/*">
                        </div>
                        <div class="tool-options">
                            <label>
                                <input type="checkbox" id="preserve-transparency" checked>
                                Preserve Transparency
                            </label>
                        </div>
                    </div>
                    <div class="tool-result" id="png-result">
                        <p>Your converted PNG image will appear here after upload.</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
    
    <!-- Other modals remain the same as previous versions -->
    
    <!-- Chatbot Container -->
    <div id="chatbot-container">
        <div id="chat-header">
            <span>Need help? Chat with us!</span>
            <span id="chat-toggle">+</span>
        </div>
        <div id="chat-body">
            <div id="chat-messages"></div>
            <div id="chat-input-container">
                <input type="text" id="user-input" placeholder="Type your message...">
                <button id="send-btn">Send</button>
            </div>
        </div>
    </div>
    
    <footer>
        <div class="footer-links">
            <a href="#">About Us</a>
            <a href="#">Contact</a>
            <a href="#">Privacy Policy</a>
            <a href="#">Terms of Service</a>
        </div>
        <div class="copyright">
            &copy; 2023 ABLUTE_MILLION. All rights reserved.
        </div>
    </footer>
    
    <script>
        // Navigation between pages
        document.querySelectorAll('.nav-link').forEach(link => {
            link.addEventListener('click', function(e) {
                e.preventDefault();
                
                // Remove active class from all links and pages
                document.querySelectorAll('.nav-link').forEach(el => el.classList.remove('active'));
                document.querySelectorAll('.page-content').forEach(el => el.classList.remove('active'));
                
                // Add active class to clicked link
                this.classList.add('active');
                
                // Show corresponding page
                const pageId = this.getAttribute('data-page');
                document.getElementById(pageId).classList.add('active');
                
                // Scroll to top
                window.scrollTo({ top: 0, behavior: 'smooth' });
            });
        });
        
        // Initialize AdSense ads
        (adsbygoogle = window.adsbygoogle || [6283374890158723"]).push({});
        
        // Modal functionality
        const modals = {
            // Image Tools
            'png-converter': document.getElementById('png-converter-modal'),
            'jpg-converter': document.getElementById('jpg-converter-modal'),
            'image-resizer': document.getElementById('image-resizer-modal'),
            'image-compressor': document.getElementById('image-compressor-modal'),
            'image-cropper': document.getElementById('image-cropper-modal'),
            'base64-converter': document.getElementById('base64-converter-modal'),
            'webp-converter': document.getElementById('webp-converter-modal'),
            'gif-maker': document.getElementById('gif-maker-modal'),
            'qr-generator': document.getElementById('qr-generator-modal'),
            
            // Social Media Tools
            'yt-thumbnail': document.getElementById('yt-thumbnail-modal')
        };
        
        // Open modals when buttons are clicked
        document.querySelectorAll('.try-tool').forEach(btn => {
            btn.addEventListener('click', function() {
                const tool = this.getAttribute('data-tool');
                document.body.style.overflow = 'hidden';
                modals[tool].style.display = 'block';
            });
        });
        
        // Close modals when X is clicked
        document.querySelectorAll('.close-modal').forEach(closeBtn => {
            closeBtn.addEventListener('click', function() {
                document.body.style.overflow = 'auto';
                this.closest('.modal').style.display = 'none';
            });
        });
        
        // Close modals when clicking outside
        window.addEventListener('click', function(e) {
            if (e.target.classList.contains('modal')) {
                document.body.style.overflow = 'auto';
                e.target.style.display = 'none';
            }
        });
        
        // Chatbot functionality
        const chatBody = document.getElementById('chat-body');
        const chatToggle = document.getElementById('chat-toggle');
        const chatMessages = document.getElementById('chat-messages');
        const userInput = document.getElementById('user-input');
        const sendBtn = document.getElementById('send-btn');
        
        let isChatOpen = false;
        
        // Toggle chat visibility
        chatToggle.addEventListener('click', toggleChat);
        
        function toggleChat() {
            isChatOpen = !isChatOpen;
            if (isChatOpen) {
                chatBody.classList.add('expanded');
                chatToggle.textContent = '−';
                userInput.focus();
            } else {
                chatBody.classList.remove('expanded');
                chatToggle.textContent = '+';
            }
        }
        
        // Send message
        sendBtn.addEventListener('click', sendMessage);
        userInput.addEventListener('keypress', (e) => {
            if (e.key === 'Enter') sendMessage();
        });
        
        // Initial greeting
        setTimeout(() => {
            addBotMessage("Hello! I'm your ABLUTE_MILLION assistant. How can I help you with our image and social media tools today?");
        }, 1500);
        
        // Enhanced responses for image tools website
        const simpleResponses = {
            "hello": ["Hello there! How can I assist you with our image tools today?", "Hi! Ready to help with any image conversion or editing needs.", "Greetings! Ask me about our image and social media tools."],
            "hi": ["Hello there! How can I assist you with our image tools today?", "Hi! Ready to help with any image conversion or editing needs.", "Greetings! Ask me about our image and social media tools."],
            "help": ["I can help you with all our image tools - converters, resizers, compressors and more!", 
                    "What would you like to know about? We have PNG/JPG converters, image resizers, QR generators and YouTube thumbnail downloaders."],
            "convert": ["We offer several conversion tools: PNG, JPG, WebP, and Base64 converters. Which one do you need?", 
                       "For image conversion, we have tools to convert between PNG, JPG, and WebP formats."],
            "png": ["Our PNG converter preserves transparency and converts any image to PNG format. Click 'Image Tools' in the menu to try it!", 
                   "To convert to PNG, use our Image to PNG converter tool under the Image Tools section."],
            "jpg": ["Our JPG converter lets you adjust quality settings when converting images. Find it under Image Tools.", 
                   "For JPG conversion with quality control, check out our Image to JPG converter."],
            "resize": ["Need to resize an image? Our Image Resizer maintains aspect ratio automatically. Try it in the Image Tools section!", 
                      "The Image Resizer tool lets you specify exact dimensions while keeping your image proportions correct."],
            "compress": ["Our Image Compressor reduces file size without noticeable quality loss. You can adjust compression level too!", 
                        "To make your images smaller for web use, try our Image Compressor under Image Tools."],
            "qr": ["Generate custom QR codes for URLs, text, or contact info with our QR Code Generator tool.", 
                  "Our QR Code Generator lets you customize size and colors. Find it in the Image Tools section."],
            "youtube": ["We have a YouTube Thumbnail Downloader in our Social Media Tools section. Just paste a YouTube URL!", 
                       "To download YouTube thumbnails, go to Social Media Tools and enter the video URL."],
            "tools": ["We offer these image tools: PNG/JPG/WebP converters, Image Resizer, Compressor, Cropper, Base64 converter, GIF Maker, and QR Generator.", 
                     "Our tools include image format converters, editing tools, and social media utilities like YouTube thumbnail downloader."],
            "instagram": ["Follow us on Instagram @official__ankit__0005 for updates and tips!", 
                         "Check out our Instagram @official__ankit__0005 for the latest tool updates and content creation tips."],
            "bye": ["Goodbye! Come back if you need help with our image tools!", "Thanks for chatting! Happy editing with ABLUTE_MILLION tools!"]
        };
        
        function sendMessage() {
            const message = userInput.value.trim();
            
            if (message) {
                // Add user message to chat
                addUserMessage(message);
                userInput.value = '';
                
                // Show typing indicator
                showTypingIndicator();
                
                // Simulate processing delay
                setTimeout(() => {
                    // Remove typing indicator
                    removeTypingIndicator();
                    
                    // Process message and get response
                    const response = getBotResponse(message);
                    addBotMessage(response);
                }, 1000 + Math.random() * 2000); // Random delay between 1-3 seconds
            }
        }
        
        function addUserMessage(message) {
            const messageDiv = document.createElement('div');
            messageDiv.className = 'user-message';
            messageDiv.innerHTML = `
                <div class="message-bubble">${message}</div>
            `;
            chatMessages.appendChild(messageDiv);
            scrollToBottom();
        }
        
        function addBotMessage(message) {
            const messageDiv = document.createElement('div');
            messageDiv.className = 'bot-message';
            messageDiv.innerHTML = `
                <div class="message-bubble">${message}</div>
            `;
            chatMessages.appendChild(messageDiv);
            scrollToBottom();
        }
        
        function showTypingIndicator() {
            const typingDiv = document.createElement('div');
            typingDiv.className = 'bot-message';
            typingDiv.id = 'typing-indicator';
            typingDiv.innerHTML = `
                <div class="typing-indicator">
                    <div class="typing-dot"></div>
                    <div class="typing-dot"></div>
                    <div class="typing-dot"></div>
                </div>
            `;
            chatMessages.appendChild(typingDiv);
            scrollToBottom();
        }
        
        function removeTypingIndicator() {
            const typingIndicator = document.getElementById('typing-indicator');
            if (typingIndicator) {
                typingIndicator.remove();
            }
        }
        
        function scrollToBottom() {
            chatMessages.scrollTop = chatMessages.scrollHeight;
        }
        
        function getBotResponse(userMessage) {
            const lowerMessage = userMessage.toLowerCase();
            
            // Check for simple responses first
            for (const [keyword, responses] of Object.entries(simpleResponses)) {
                if (lowerMessage.includes(keyword)) {
                    return responses[Math.floor(Math.random() * responses.length)];
                }
            }
            
            // Default responses
            const defaultResponses = [
                "I'm not sure I understand. Could you rephrase your question about our image tools?",
                "I can help with questions about our image conversion and editing tools. Could you be more specific?",
                "I'm still learning about all our tools. Could you ask me about something else?",
                "I don't have the answer to that right now, but I can help with questions about our PNG/JPG converters, image resizer, or other tools."
            ];
            
            return defaultResponses[Math.floor(Math.random() * defaultResponses.length)];
        }
        
        // File upload handlers for all tools (simulated processing)
        document.querySelectorAll('.file-upload').forEach(upload => {
            upload.addEventListener('click', function() {
                this.querySelector('input[type="file"]').click();
            });
        });
        
        document.querySelectorAll('input[type="file"]').forEach(input => {
            input.addEventListener('change', function(e) {
                const file = e.target.files[0];
                if (!file) return;
                
                const toolId = this.id.replace('-file-input', '');
                const resultDiv = document.getElementById(`${toolId}-result`);
                
                // Show loading state
                resultDiv.innerHTML = '<p>Processing file... <span class="spinner"></span></p>';
                
                // Simulate processing delay
                setTimeout(() => {
                    // Create preview for image tools
                    if (toolId !== 'base64') {
                        const reader = new FileReader();
                        reader.onload = function(event) {
                            if (toolId === 'gif') {
                                // Handle multiple files for GIF maker
                                const files = e.target.files;
                                if (files.length < 2) {
                                    resultDiv.innerHTML = '<p>Please select at least 2 images to create a GIF</p>';
                                    return;
                                }
                                
                                let previewHTML = '<p>Selected images for GIF:</p><div style="display: flex; flex-wrap: wrap; gap: 0.5rem; margin: 1rem 0;">';
                                for (let i = 0; i < Math.min(files.length, 5); i++) {
                                    previewHTML += `<img src="${URL.createObjectURL(files[i])}" style="height: 80px; border-radius: 5px;">`;
                                }
                                if (files.length > 5) previewHTML += `<p>+ ${files.length - 5} more</p>`;
                                previewHTML += '</div><button class="btn create-gif">Create GIF</button>';
                                
                                resultDiv.innerHTML = previewHTML;
                                
                                // Add create GIF button handler
                                document.querySelector('.create-gif')?.addEventListener('click', function() {
                                    resultDiv.innerHTML = '<p>Creating GIF... <span class="spinner"></span></p>';
                                    
                                    setTimeout(() => {
                                        // Simulated GIF creation
                                        resultDiv.innerHTML = `
                                            <p>Your GIF is ready!</p>
                                            <img src="https://media.giphy.com/media/3o7TKSha51ATTx9KzC/giphy.gif" style="max-width: 100%; border-radius: 8px;">
                                            <button class="btn download-gif">Download GIF</button>
                                        `;
                                        
                                        // Add download handler
                                        document.querySelector('.download-gif')?.addEventListener('click', function() {
                                            alert('In a real implementation, this would download the generated GIF');
                                        });
                                    }, 2000);
                                });
                            } else if (toolId === 'crop') {
                                // Show crop preview
                                resultDiv.querySelector('p').textContent = 'Drag the selection to choose crop area';
                                document.getElementById('crop-preview-container').style.display = 'block';
                                document.getElementById('crop-preview').src = event.target.result;
                            } else {
                                // Show processed image
                                resultDiv.innerHTML = `
                                    <p>Processed image:</p>
                                    <img src="${event.target.result}" style="max-width: 100%; border-radius: 8px;">
                                    <button class="btn download-${toolId}">Download Image</button>
                                `;
                                
                                // Add download handler
                                document.querySelector(`.download-${toolId}`)?.addEventListener('click', function() {
                                    alert('In a real implementation, this would download the processed image');
                                });
                            }
                        };
                        
                        if (toolId === 'gif') {
                            // For GIF maker, we handle multiple files in the click handler
                            resultDiv.innerHTML = '<p>Selected ' + e.target.files.length + ' files for GIF creation</p>';
                        } else {
                            reader.readAsDataURL(file);
                        }
                    }
                }, 1000);
            });
        });
    </script>
</body>
</html>
