<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ToolifyWorld - 2025 Free AI Tools Hub</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }

        :root {
            --primary: #4361ee;
            --secondary: #3a0ca3;
            --accent: #f72585;
            --light: #f8f9fa;
            --dark: #212529;
            --success: #4cc9f0;
            --warning: #ffd166;
            --danger: #ef476f;
            --gray: #6c757d;
            --bg-light: #ffffff;
            --bg-dark: #121212;
            --text-light: #212529;
            --text-dark: #f8f9fa;
        }

        body {
            background-color: var(--bg-light);
            color: var(--text-light);
            transition: background-color 0.3s, color 0.3s;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
        }

        body.dark-mode {
            background-color: var(--bg-dark);
            color: var(--text-dark);
        }

        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }

        /* Header Styles */
        header {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 1.5rem;
            font-weight: 700;
        }

        .logo i {
            color: var(--warning);
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 20px;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }

        nav a:hover {
            color: var(--warning);
        }

        .auth-buttons {
            display: flex;
            gap: 10px;
        }

        .btn {
            padding: 8px 16px;
            border-radius: 50px;
            border: none;
            cursor: pointer;
            font-weight: 500;
            transition: all 0.3s;
        }

        .btn-outline {
            background: transparent;
            border: 2px solid white;
            color: white;
        }

        .btn-outline:hover {
            background: white;
            color: var(--primary);
        }

        .btn-primary {
            background: var(--accent);
            color: white;
        }

        .btn-primary:hover {
            background: #d81159;
        }

        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* Hero Section */
        .hero {
            padding: 80px 0;
            text-align: center;
            background: linear-gradient(rgba(67, 97, 238, 0.1), rgba(58, 12, 163, 0.1));
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 20px;
            background: linear-gradient(135deg, var(--primary), var(--accent));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero p {
            font-size: 1.2rem;
            color: var(--gray);
            max-width: 700px;
            margin: 0 auto 30px;
        }

        /* Tools Grid */
        .section-title {
            text-align: center;
            margin: 50px 0 30px;
            font-size: 2rem;
            color: var(--primary);
        }

        .tools-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
            padding: 20px;
        }

        .tool-card {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s, box-shadow 0.3s;
            cursor: pointer;
        }

        body.dark-mode .tool-card {
            background: #1e1e1e;
            box-shadow: 0 5px 15px rgba(255, 255, 255, 0.05);
        }

        .tool-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
        }

        .tool-card-header {
            padding: 20px;
            text-align: center;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
        }

        .tool-card-header i {
            font-size: 2.5rem;
            margin-bottom: 10px;
        }

        .tool-card-body {
            padding: 20px;
        }

        .tool-card-body h3 {
            margin-bottom: 10px;
            color: var(--primary);
        }

        body.dark-mode .tool-card-body h3 {
            color: var(--warning);
        }

        .tool-card-body p {
            color: var(--gray);
            margin-bottom: 15px;
        }

        /* Features Section */
        .features {
            padding: 50px 0;
            background-color: rgba(67, 97, 238, 0.05);
        }

        body.dark-mode .features {
            background-color: rgba(255, 255, 255, 0.05);
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
        }

        .feature-card {
            background: white;
            padding: 25px;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            text-align: center;
        }

        body.dark-mode .feature-card {
            background: #1e1e1e;
            box-shadow: 0 5px 15px rgba(255, 255, 255, 0.05);
        }

        .feature-card i {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 15px;
        }

        /* Footer */
        footer {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 40px 0 20px;
            margin-top: 50px;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }

        .footer-section h3 {
            margin-bottom: 20px;
            font-size: 1.3rem;
        }

        .footer-section ul {
            list-style: none;
        }

        .footer-section ul li {
            margin-bottom: 10px;
        }

        .footer-section a {
            color: rgba(255, 255, 255, 0.8);
            text-decoration: none;
            transition: color 0.3s;
        }

        .footer-section a:hover {
            color: var(--warning);
        }

        .social-icons {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }

        .social-icons a {
            color: white;
            font-size: 1.5rem;
        }

        .copyright {
            text-align: center;
            margin-top: 40px;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .header-content {
                flex-wrap: wrap;
            }

            nav {
                width: 100%;
                order: 3;
                margin-top: 15px;
                display: none;
            }

            nav.active {
                display: block;
            }

            nav ul {
                flex-direction: column;
                gap: 10px;
            }

            .mobile-menu-btn {
                display: block;
            }

            .auth-buttons {
                margin-left: auto;
            }

            .hero h1 {
                font-size: 2.2rem;
            }

            .hero p {
                font-size: 1rem;
            }
        }

        /* Tool Modals */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.7);
            z-index: 1001;
            overflow-y: auto;
            padding: 20px;
        }

        .modal-content {
            background: white;
            margin: 50px auto;
            max-width: 600px;
            border-radius: 12px;
            box-shadow: 0 5px 30px rgba(0, 0, 0, 0.3);
            position: relative;
        }

        body.dark-mode .modal-content {
            background: #1e1e1e;
        }

        .close-modal {
            position: absolute;
            top: 15px;
            right: 15px;
            font-size: 1.5rem;
            color: var(--gray);
            background: none;
            border: none;
            cursor: pointer;
        }

        .modal-header {
            padding: 20px;
            border-bottom: 1px solid #eee;
            text-align: center;
        }

        body.dark-mode .modal-header {
            border-bottom: 1px solid #333;
        }

        .modal-body {
            padding: 20px;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
        }

        .form-control {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 8px;
            font-size: 1rem;
        }

        body.dark-mode .form-control {
            background: #2d2d2d;
            border-color: #444;
            color: white;
        }

        textarea.form-control {
            min-height: 120px;
            resize: vertical;
        }

        .tool-result {
            margin-top: 20px;
            padding: 15px;
            border-radius: 8px;
            background: #f8f9fa;
            min-height: 100px;
        }

        body.dark-mode .tool-result {
            background: #2d2d2d;
        }

        /* Language Selector */
        .language-selector {
            position: relative;
            display: inline-block;
            margin-left: 20px;
        }

        .language-btn {
            background: rgba(255, 255, 255, 0.2);
            color: white;
            padding: 8px 15px;
            border-radius: 50px;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 5px;
        }

        .language-dropdown {
            display: none;
            position: absolute;
            top: 100%;
            left: 0;
            background: white;
            min-width: 150px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            border-radius: 8px;
            overflow: hidden;
            z-index: 1000;
        }

        body.dark-mode .language-dropdown {
            background: #2d2d2d;
        }

        .language-dropdown a {
            display: block;
            padding: 10px 15px;
            color: var(--dark);
            text-decoration: none;
            transition: background 0.3s;
        }

        body.dark-mode .language-dropdown a {
            color: white;
        }

        .language-dropdown a:hover {
            background: rgba(67, 97, 238, 0.1);
        }

        .language-selector:hover .language-dropdown {
            display: block;
        }

        /* Dark Mode Toggle */
        .dark-mode-toggle {
            margin-left: 20px;
            background: none;
            border: none;
            color: white;
            font-size: 1.2rem;
            cursor: pointer;
        }

        /* QR Code Output */
        #qrcode {
            text-align: center;
            margin: 20px 0;
        }

        #qrcode canvas {
            border: 1px solid #ddd;
            border-radius: 8px;
            padding: 10px;
            background: white;
        }

        /* Resume Preview */
        .resume-preview {
            border: 1px solid #ddd;
            border-radius: 8px;
            padding: 20px;
            margin-top: 20px;
            background: white;
            min-height: 300px;
        }

        body.dark-mode .resume-preview {
            background: #2d2d2d;
            border-color: #444;
        }

        .resume-header {
            text-align: center;
            margin-bottom: 20px;
        }

        .resume-section {
            margin-bottom: 15px;
        }

        /* Loading Spinner */
        .spinner {
            display: none;
            border: 4px solid rgba(0, 0, 0, 0.1);
            border-left: 4px solid var(--primary);
            border-radius: 50%;
            width: 30px;
            height: 30px;
            animation: spin 1s linear infinite;
            margin: 20px auto;
        }

        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        /* Login Modal */
        .auth-modal .modal-content {
            max-width: 400px;
        }

        .auth-tabs {
            display: flex;
            border-bottom: 1px solid #ddd;
        }

        .auth-tab {
            flex: 1;
            text-align: center;
            padding: 15px;
            cursor: pointer;
            background: #f8f9fa;
        }

        body.dark-mode .auth-tab {
            background: #2d2d2d;
        }

        .auth-tab.active {
            background: white;
            border-bottom: 2px solid var(--primary);
        }

        body.dark-mode .auth-tab.active {
            background: #1e1e1e;
        }

        .auth-form {
            padding: 20px;
        }

        .auth-form .form-group {
            margin-bottom: 15px;
        }

        .social-auth {
            text-align: center;
            margin-top: 20px;
        }

        .social-buttons {
            display: flex;
            gap: 10px;
            margin-top: 10px;
        }

        .social-btn {
            flex: 1;
            padding: 10px;
            border-radius: 5px;
            border: none;
            cursor: pointer;
            color: white;
        }

        .google-btn {
            background: #DB4437;
        }

        .facebook-btn {
            background: #4267B2;
        }

        /* Image Gallery */
        .image-gallery {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
            gap: 15px;
            margin-top: 20px;
        }

        .image-item {
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.2);
            transition: transform 0.3s;
        }

        .image-item:hover {
            transform: scale(1.05);
        }

        .image-item img {
            width: 100%;
            height: 150px;
            object-fit: cover;
            display: block;
        }

        /* Publish Instructions */
        .publish-instructions {
            background: white;
            border-radius: 12px;
            padding: 25px;
            margin: 40px 0;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        body.dark-mode .publish-instructions {
            background: #1e1e1e;
        }

        .publish-instructions h2 {
            color: var(--primary);
            margin-bottom: 20px;
            text-align: center;
        }

        .instructions-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }

        .instruction-card {
            background: #f8f9fa;
            padding: 20px;
            border-radius: 8px;
            text-align: center;
        }

        body.dark-mode .instruction-card {
            background: #2d2d2d;
        }

        .instruction-card i {
            font-size: 2rem;
            color: var(--primary);
            margin-bottom: 15px;
        }

        .instruction-card h3 {
            margin-bottom: 10px;
            color: var(--dark);
        }

        body.dark-mode .instruction-card h3 {
            color: white;
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-content">
            <div class="logo">
                <i class="fas fa-tools"></i>
                <span>ToolifyWorld</span>
            </div>

            <nav id="nav">
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#tools">Tools</a></li>
                    <li><a href="#features">Features</a></li>
                    <li><a href="#publish">Publish</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>

            <div class="auth-buttons">
                <button class="btn btn-outline" id="loginBtn">Login</button>
                <button class="btn btn-primary" id="signupBtn">Sign Up</button>
            </div>

            <div class="language-selector">
                <div class="language-btn">
                    <i class="fas fa-globe"></i>
                    <span>English</span>
                    <i class="fas fa-chevron-down"></i>
                </div>
                <div class="language-dropdown">
                    <a href="#" data-lang="en">English</a>
                    <a href="#" data-lang="bn">Bengali</a>
                    <a href="#" data-lang="hi">Hindi</a>
                    <a href="#" data-lang="ar">Arabic</a>
                    <a href="#" data-lang="es">Spanish</a>
                </div>
            </div>

            <button class="dark-mode-toggle" id="darkModeToggle">
                <i class="fas fa-moon"></i>
            </button>

            <button class="mobile-menu-btn" id="mobileMenuBtn">
                <i class="fas fa-bars"></i>
            </button>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <h1>Free AI-Powered Tools for Everyone</h1>
            <p>Access a suite of powerful tools for content creation, translation, code generation, and more - completely free in 2025!</p>
            <button class="btn btn-primary">Get Started</button>
        </div>
    </section>

    <!-- Tools Section -->
    <section id="tools">
        <h2 class="section-title">Our Tools</h2>
        <div class="container tools-grid">
            <!-- AI Tools Hub -->
            <div class="tool-card" data-tool="ai-tools">
                <div class="tool-card-header">
                    <i class="fas fa-robot"></i>
                    <h3>AI Tools Hub</h3>
                </div>
                <div class="tool-card-body">
                    <p>Access a collection of AI-powered tools for various tasks including content generation, summarization, and more.</p>
                    <button class="btn btn-primary">Use Tool</button>
                </div>
            </div>

            <!-- QR/Barcode Generator -->
            <div class="tool-card" data-tool="qr-generator">
                <div class="tool-card-header">
                    <i class="fas fa-qrcode"></i>
                    <h3>QR/Barcode Generator</h3>
                </div>
                <div class="tool-card-body">
                    <p>Create QR codes and barcodes for URLs, contact information, products, and more in seconds.</p>
                    <button class="btn btn-primary">Use Tool</button>
                </div>
            </div>

            <!-- Resume Builder -->
            <div class="tool-card" data-tool="resume-builder">
                <div class="tool-card-header">
                    <i class="fas fa-file-alt"></i>
                    <h3>Resume Builder</h3>
                </div>
                <div class="tool-card-body">
                    <p>Create professional resumes with our easy-to-use builder. Multiple templates available.</p>
                    <button class="btn btn-primary">Use Tool</button>
                </div>
            </div>

            <!-- AI Text Generator -->
            <div class="tool-card" data-tool="ai-text">
                <div class="tool-card-header">
                    <i class="fas fa-font"></i>
                    <h3>AI Text Generator</h3>
                </div>
                <div class="tool-card-body">
                    <p>Generate high-quality content for articles, stories, emails, and more with our AI text generator.</p>
                    <button class="btn btn-primary">Use Tool</button>
                </div>
            </div>

            <!-- AI Image Generator -->
            <div class="tool-card" data-tool="ai-image">
                <div class="tool-card-header">
                    <i class="fas fa-image"></i>
                    <h3>AI Image Generator</h3>
                </div>
                <div class="tool-card-body">
                    <p>Create stunning images from text descriptions using our AI image generation technology.</p>
                    <button class="btn btn-primary">Use Tool</button>
                </div>
            </div>

            <!-- Translator -->
            <div class="tool-card" data-tool="translator">
                <div class="tool-card-header">
                    <i class="fas fa-language"></i>
                    <h3>Translator</h3>
                </div>
                <div class="tool-card-body">
                    <p>Translate text between multiple languages with high accuracy using our translation tool.</p>
                    <button class="btn btn-primary">Use Tool</button>
                </div>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section class="features" id="features">
        <div class="container">
            <h2 class="section-title">Why Choose ToolifyWorld?</h2>
            <div class="features-grid">
                <div class="feature-card">
                    <i class="fas fa-lock"></i>
                    <h3>Safe for All</h3>
                    <p>Our tools are designed with safety and privacy in mind, ensuring a secure experience for all users.</p>
                </div>
                <div class="feature-card">
                    <i class="fas fa-mobile-alt"></i>
                    <h3>Fully Responsive</h3>
                    <p>Access our tools from any device - desktop, tablet, or mobile - with our responsive design.</p>
                </div>
                <div class="feature-card">
                    <i class="fas fa-user-shield"></i>
                    <h3>User Accounts</h3>
                    <p>Create an account to save your work, track usage history, and access additional features.</p>
                </div>
                <div class="feature-card">
                    <i class="fas fa-globe-americas"></i>
                    <h3>Multi-Language</h3>
                    <p>Use our tools in multiple languages with more being added regularly.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Publish Instructions -->
    <section class="publish-instructions" id="publish">
        <div class="container">
            <h2>How to Publish Your Site for Free</h2>
            <div class="instructions-grid">
                <div class="instruction-card">
                    <i class="fab fa-github"></i>
                    <h3>GitHub Pages</h3>
                    <p>Create a GitHub repository, upload your files, and enable GitHub Pages in settings.</p>
                </div>
                <div class="instruction-card">
                    <i class="fab fa-netlify"></i>
                    <h3>Netlify</h3>
                    <p>Drag and drop your folder or connect your GitHub repository for automatic deployment.</p>
                </div>
                <div class="instruction-card">
                    <i class="fab fa-vercel"></i>
                    <h3>Vercel</h3>
                    <p>Import your project from GitHub, GitLab, or Bitbucket for seamless deployment.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer id="contact">
        <div class="container footer-content">
            <div class="footer-section">
                <h3>ToolifyWorld</h3>
                <p>Providing free AI-powered tools to users worldwide since 2023.</p>
                <div class="social-icons">
                    <a href="#"><i class="fab fa-facebook"></i></a>
                    <a href="#"><i class="fab fa-twitter"></i></a>
                    <a href="#"><i class="fab fa-instagram"></i></a>
                    <a href="#"><i class="fab fa-linkedin"></i></a>
                </div>
            </div>
            <div class="footer-section">
                <h3>Quick Links</h3>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#tools">Tools</a></li>
                    <li><a href="#features">Features</a></li>
                    <li><a href="#publish">Publish Guide</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </div>
            <div class="footer-section">
                <h3>Legal</h3>
                <ul>
                    <li><a href="#">Privacy Policy</a></li>
                    <li><a href="#">Terms of Service</a></li>
                    <li><a href="#">Cookie Policy</a></li>
                    <li><a href="#">GDPR Compliance</a></li>
                </ul>
            </div>
            <div class="footer-section">
                <h3>Contact Us</h3>
                <ul>
                    <li><i class="fas fa-envelope"></i> support@toolifyworld.com</li>
                    <li><i class="fas fa-phone"></i> +1 (555) 123-4567</li>
                    <li><i class="fas fa-map-marker-alt"></i> Global Remote Team</li>
                </ul>
            </div>
        </div>
        <div class="copyright">
            <p>&copy; 2023-2025 ToolifyWorld. All rights reserved.</p>
        </div>
    </footer>

    <!-- Tool Modals -->
    <!-- AI Tools Modal -->
    <div class="modal" id="ai-tools-modal">
        <div class="modal-content">
            <button class="close-modal">&times;</button>
            <div class="modal-header">
                <h2>AI Tools Hub</h2>
            </div>
            <div class="modal-body">
                <div class="form-group">
                    <label for="ai-tool-select">Choose Tool:</label>
                    <select id="ai-tool-select" class="form-control">
                        <option value="text-summarizer">Text Summarizer</option>
                        <option value="content-rewriter">Content Rewriter</option>
                        <option value="code-generator">Code Generator</option>
                        <option value="sentiment-analysis">Sentiment Analysis</option>
                    </select>
                </div>
                <div class="form-group">
                    <label for="ai-input">Input:</label>
                    <textarea id="ai-input" class="form-control" rows="5" placeholder="Enter your text here..."></textarea>
                </div>
                <button class="btn btn-primary" id="generate-ai">Generate</button>
                <div class="spinner" id="ai-spinner"></div>
                <div class="tool-result" id="ai-result"></div>
            </div>
        </div>
    </div>

    <!-- QR Generator Modal -->
    <div class="modal" id="qr-generator-modal">
        <div class="modal-content">
            <button class="close-modal">&times;</button>
            <div class="modal-header">
                <h2>QR/Barcode Generator</h2>
            </div>
            <div class="modal-body">
                <div class="form-group">
                    <label for="qr-type">Type:</label>
                    <select id="qr-type" class="form-control">
                        <option value="url">URL</option>
                        <option value="text">Text</option>
                        <option value="email">Email</option>
                        <option value="wifi">Wi-Fi</option>
                    </select>
                </div>
                <div class="form-group">
                    <label for="qr-content">Content:</label>
                    <input type="text" id="qr-content" class="form-control" placeholder="Enter content here...">
                </div>
                <button class="btn btn-primary" id="generate-qr">Generate QR Code</button>
                <div id="qrcode"></div>
            </div>
        </div>
    </div>

    <!-- Resume Builder Modal -->
    <div class="modal" id="resume-builder-modal">
        <div class="modal-content">
            <button class="close-modal">&times;</button>
            <div class="modal-header">
                <h2>Resume Builder</h2>
            </div>
            <div class="modal-body">
                <div class="form-group">
                    <label for="resume-name">Full Name:</label>
                    <input type="text" id="resume-name" class="form-control" placeholder="Your full name">
                </div>
                <div class="form-group">
                    <label for="resume-email">Email:</label>
                    <input type="email" id="resume-email" class="form-control" placeholder="Your email">
                </div>
                <div class="form-group">
                    <label for="resume-phone">Phone:</label>
                    <input type="tel" id="resume-phone" class="form-control" placeholder="Your phone number">
                </div>
                <div class="form-group">
                    <label for="resume-experience">Work Experience:</label>
                    <textarea id="resume-experience" class="form-control" rows="3" placeholder="Describe your work experience"></textarea>
                </div>
                <div class="form-group">
                    <label for="resume-education">Education:</label>
                    <textarea id="resume-education" class="form-control" rows="3" placeholder="Your educational background"></textarea>
                </div>
                <div class="form-group">
                    <label for="resume-skills">Skills:</label>
                    <input type="text" id="resume-skills" class="form-control" placeholder="List your skills (comma separated)">
                </div>
                <button class="btn btn-primary" id="generate-resume">Generate Resume</button>
                
                <div class="resume-preview" id="resume-preview">
                    <p class="text-center">Your resume will appear here</p>
                </div>
            </div>
        </div>
    </div>

    <!-- AI Text Generator Modal -->
    <div class="modal" id="ai-text-modal">
        <div class="modal-content">
            <button class="close-modal">&times;</button>
            <div class="modal-header">
                <h2>AI Text Generator</h2>
            </div>
            <div class="modal-body">
                <div class="form-group">
                    <label for="text-type">Text Type:</label>
                    <select id="text-type" class="form-control">
                        <option value="article">Article/Blog Post</option>
                        <option value="story">Short Story</option>
                        <option value="email">Email</option>
                        <option value="summary">Summary</option>
                    </select>
                </div>
                <div class="form-group">
                    <label for="text-topic">Topic/Subject:</label>
                    <input type="text" id="text-topic" class="form-control" placeholder="Enter topic or subject">
                </div>
                <div class="form-group">
                    <label for="text-keywords">Keywords (optional):</label>
                    <input type="text" id="text-keywords" class="form-control" placeholder="Comma separated keywords">
                </div>
                <button class="btn btn-primary" id="generate-text">Generate Text</button>
                <div class="spinner" id="text-spinner"></div>
                <div class="tool-result" id="text-result"></div>
            </div>
        </div>
    </div>

    <!-- AI Image Generator Modal -->
    <div class="modal" id="ai-image-modal">
        <div class="modal-content">
            <button class="close-modal">&times;</button>
            <div class="modal-header">
                <h2>AI Image Generator</h2>
            </div>
            <div class="modal-body">
                <div class="form-group">
                    <label for="image-prompt">Image Description:</label>
                    <textarea id="image-prompt" class="form-control" rows="3" placeholder="Describe the image you want to generate..."></textarea>
                </div>
                <div class="form-group">
                    <label for="image-style">Style:</label>
                    <select id="image-style" class="form-control">
                        <option value="realistic">Realistic</option>
                        <option value="cartoon">Cartoon</option>
                        <option value="abstract">Abstract</option>
                        <option value="painting">Painting</option>
                    </select>
                </div>
                <button class="btn btn-primary" id="generate-image">Generate Image</button>
                <div class="spinner" id="image-spinner"></div>
                <div class="tool-result" id="image-result">
                    <div class="image-gallery" id="image-gallery">
                        <!-- Generated images will appear here -->
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Translator Modal -->
    <div class="modal" id="translator-modal">
        <div class="modal-content">
            <button class="close-modal">&times;</button>
            <div class="modal-header">
                <h2>Translator</h2>
            </div>
            <div class="modal-body">
                <div class="form-group">
                    <label for="source-lang">From:</label>
                    <select id="source-lang" class="form-control">
                        <option value="en">English</option>
                        <option value="bn">Bengali</option>
                        <option value="hi">Hindi</option>
                        <option value="ar">Arabic</option>
                        <option value="es">Spanish</option>
                    </select>
                </div>
                <div class="form-group">
                    <label for="target-lang">To:</label>
                    <select id="target-lang" class="form-control">
                        <option value="en">English</option>
                        <option value="bn">Bengali</option>
                        <option value="hi">Hindi</option>
                        <option value="ar">Arabic</option>
                        <option value="es">Spanish</option>
                    </select>
                </div>
                <div class="form-group">
                    <label for="translate-text">Text to Translate:</label>
                    <textarea id="translate-text" class="form-control" rows="4" placeholder="Enter text to translate"></textarea>
                </div>
                <button class="btn btn-primary" id="translate-btn">Translate</button>
                <div class="spinner" id="translate-spinner"></div>
                <div class="tool-result" id="translation-result"></div>
            </div>
        </div>
    </div>

    <!-- Login/Signup Modal -->
    <div class="modal auth-modal" id="auth-modal">
        <div class="modal-content">
            <button class="close-modal">&times;</button>
            <div class="auth-tabs">
                <div class="auth-tab active" id="login-tab">Login</div>
                <div class="auth-tab" id="signup-tab">Sign Up</div>
            </div>
            <div class="auth-form">
                <div id="login-form">
                    <div class="form-group">
                        <label for="login-email">Email:</label>
                        <input type="email" id="login-email" class="form-control" placeholder="Your email">
                    </div>
                    <div class="form-group">
                        <label for="login-password">Password:</label>
                        <input type="password" id="login-password" class="form-control" placeholder="Your password">
                    </div>
                    <button class="btn btn-primary btn-block">Login</button>
                    
                    <div class="social-auth">
                        <p>Or login with:</p>
                        <div class="social-buttons">
                            <button class="social-btn google-btn">Google</button>
                            <button class="social-btn facebook-btn">Facebook</button>
                        </div>
                    </div>
                </div>
                
                <div id="signup-form" style="display: none;">
                    <div class="form-group">
                        <label for="signup-name">Full Name:</label>
                        <input type="text" id="signup-name" class="form-control" placeholder="Your full name">
                    </div>
                    <div class="form-group">
                        <label for="signup-email">Email:</label>
                        <input type="email" id="signup-email" class="form-control" placeholder="Your email">
                    </div>
                    <div class="form-group">
                        <label for="signup-password">Password:</label>
                        <input type="password" id="signup-password" class="form-control" placeholder="Create a password">
                    </div>
                    <div class="form-group">
                        <label for="signup-confirm">Confirm Password:</label>
                        <input type="password" id="signup-confirm" class="form-control" placeholder="Confirm your password">
                    </div>
                    <button class="btn btn-primary btn-block">Sign Up</button>
                    
                    <div class="social-auth">
                        <p>Or sign up with:</p>
                        <div class="social-buttons">
                            <button class="social-btn google-btn">Google</button>
                            <button class="social-btn facebook-btn">Facebook</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- JavaScript -->
    <script>
        // DOM Elements
        const mobileMenuBtn = document.getElementById('mobileMenuBtn');
        const nav = document.getElementById('nav');
        const darkModeToggle = document.getElementById('darkModeToggle');
        const toolCards = document.querySelectorAll('.tool-card');
        const modals = document.querySelectorAll('.modal');
        const closeModalButtons = document.querySelectorAll('.close-modal');
        const languageLinks = document.querySelectorAll('.language-dropdown a');
        const loginBtn = document.getElementById('loginBtn');
        const signupBtn = document.getElementById('signupBtn');
        const loginTab = document.getElementById('login-tab');
        const signupTab = document.getElementById('signup-tab');
        const loginForm = document.getElementById('login-form');
        const signupForm = document.getElementById('signup-form');

        // Mobile Menu Toggle
        mobileMenuBtn.addEventListener('click', () => {
            nav.classList.toggle('active');
        });

        // Dark Mode Toggle
        darkModeToggle.addEventListener('click', () => {
            document.body.classList.toggle('dark-mode');
            const icon = darkModeToggle.querySelector('i');
            if (document.body.classList.contains('dark-mode')) {
                icon.classList.remove('fa-moon');
                icon.classList.add('fa-sun');
                localStorage.setItem('darkMode', 'enabled');
            } else {
                icon.classList.remove('fa-sun');
                icon.classList.add('fa-moon');
                localStorage.setItem('darkMode', 'disabled');
            }
        });

        // Check for saved dark mode preference
        if (localStorage.getItem('darkMode') === 'enabled') {
            document.body.classList.add('dark-mode');
            darkModeToggle.querySelector('i').classList.remove('fa-moon');
            darkModeToggle.querySelector('i').classList.add('fa-sun');
        }

        // Tool Card Click - Open Modal
        toolCards.forEach(card => {
            card.addEventListener('click', () => {
                const toolType = card.getAttribute('data-tool');
                const modal = document.getElementById(`${toolType}-modal`);
                if (modal) {
                    modal.style.display = 'block';
                    
                    // Special initialization for image generator
                    if (toolType === 'ai-image') {
                        initImageGallery();
                    }
                }
            });
        });

        // Close Modal
        closeModalButtons.forEach(button => {
            button.addEventListener('click', () => {
                const modal = button.closest('.modal');
                modal.style.display = 'none';
            });
        });

        // Close modal when clicking outside
        window.addEventListener('click', (e) => {
            modals.forEach(modal => {
                if (e.target === modal) {
                    modal.style.display = 'none';
                }
            });
        });

        // Language Selection
        languageLinks.forEach(link => {
            link.addEventListener('click', (e) => {
                e.preventDefault();
                const lang = link.getAttribute('data-lang');
                document.querySelector('.language-btn span').textContent = link.textContent;
                alert(`Language changed to ${link.textContent}. Actual translation would be implemented with i18n.`);
            });
        });

        // Auth Modal Tabs
        loginBtn.addEventListener('click', () => {
            document.getElementById('auth-modal').style.display = 'block';
        });

        signupBtn.addEventListener('click', () => {
            document.getElementById('auth-modal').style.display = 'block';
            signupTab.click();
        });

        loginTab.addEventListener('click', () => {
            loginTab.classList.add('active');
            signupTab.classList.remove('active');
            loginForm.style.display = 'block';
            signupForm.style.display = 'none';
        });

        signupTab.addEventListener('click', () => {
            signupTab.classList.add('active');
            loginTab.classList.remove('active');
            signupForm.style.display = 'block';
            loginForm.style.display = 'none';
        });

        // QR Code Generation
        document.getElementById('generate-qr').addEventListener('click', () => {
            const type = document.getElementById('qr-type').value;
            const content = document.getElementById('qr-content').value;
            
            if (!content) {
                alert('Please enter content to generate QR code');
                return;
            }
            
            // Clear previous QR code
            document.getElementById('qrcode').innerHTML = '';
            
            // Generate QR code
            const qrCode = document.createElement('div');
            // In a real implementation, we would use a QR code library
            qrCode.innerHTML = `
                <div style="text-align:center;">
                    <div style="width:200px; height:200px; background:#eee; margin:0 auto; display:flex; align-items:center; justify-content:center; border-radius:8px;">
                        <i class="fas fa-qrcode" style="font-size:100px; color:#333;"></i>
                    </div>
                    <p style="margin-top:10px;">QR Code for: ${content}</p>
                    <p><small>Note: This is a preview. Actual QR code generation would use a library.</small></p>
                </div>
            `;
            document.getElementById('qrcode').appendChild(qrCode);
        });

        // Resume Builder
        document.getElementById('generate-resume').addEventListener('click', () => {
            const name = document.getElementById('resume-name').value || 'Your Name';
            const email = document.getElementById('resume-email').value || 'email@example.com';
            const phone = document.getElementById('resume-phone').value || '(123) 456-7890';
            const experience = document.getElementById('resume-experience').value || 'Work experience not specified';
            const education = document.getElementById('resume-education').value || 'Education background not specified';
            const skills = document.getElementById('resume-skills').value || 'Skills not specified';
            
            const resumeHTML = `
                <div class="resume-header">
                    <h2>${name}</h2>
                    <p>${email} | ${phone}</p>
                </div>
                <div class="resume-section">
                    <h3>Work Experience</h3>
                    <p>${experience}</p>
                </div>
                <div class="resume-section">
                    <h3>Education</h3>
                    <p>${education}</p>
                </div>
                <div class="resume-section">
                    <h3>Skills</h3>
                    <p>${skills}</p>
                </div>
            `;
            
            document.getElementById('resume-preview').innerHTML = resumeHTML;
        });

        // AI Text Generator
        document.getElementById('generate-text').addEventListener('click', () => {
            const type = document.getElementById('text-type').value;
            const topic = document.getElementById('text-topic').value;
            const keywords = document.getElementById('text-keywords').value;
            
            if (!topic) {
                alert('Please enter a topic');
                return;
            }
            
            document.getElementById('text-spinner').style.display = 'block';
            document.getElementById('text-result').innerHTML = '';
            
            // Simulate API call delay
            setTimeout(() => {
                document.getElementById('text-spinner').style.display = 'none';
                
                // Generate sample text based on type
                let generatedText = '';
                
                switch(type) {
                    case 'article':
                        generatedText = `<h3>${topic}</h3><p>This is a comprehensive article about ${topic}. ${topic} is a fascinating subject that has garnered significant attention in recent years. In this article, we will explore various aspects of ${topic} and its impact on our daily lives.</p><p>There are many perspectives to consider when discussing ${topic}. From historical significance to modern applications, ${topic} continues to be relevant in today's world.</p>`;
                        break;
                    case 'story':
                        generatedText = `<h3>The Story of ${topic}</h3><p>Once upon a time, there was ${topic}. ${topic} had always been curious about the world and embarked on an adventure to discover its secrets.</p><p>Along the way, ${topic} encountered challenges and made new friends. This is the story of how ${topic} learned valuable lessons about life and friendship.</p>`;
                        break;
                    case 'email':
                        generatedText = `<p><strong>Subject:</strong> Regarding ${topic}</p><p>Dear Recipient,</p><p>I am writing to you today to discuss ${topic}. This matter is of importance because...</p><p>I would appreciate your thoughts on this topic. Please let me know when you might be available to discuss further.</p><p>Best regards,<br>Your Name</p>`;
                        break;
                    case 'summary':
                        generatedText = `<h3>Summary of ${topic}</h3><p>${topic} can be summarized as follows: It is a subject that encompasses various aspects and dimensions. The key points to remember about ${topic} are its significance, applications, and future potential.</p><p>In conclusion, ${topic} represents an important area worthy of further exploration and understanding.</p>`;
                        break;
                }
                
                if (keywords) {
                    generatedText += `<p><em>Keywords: ${keywords}</em></p>`;
                }
                
                document.getElementById('text-result').innerHTML = generatedText;
            }, 1500);
        });

        // AI Image Generator
        function initImageGallery() {
            // Preload some sample images for the gallery
            const imageGallery = document.getElementById('image-gallery');
            imageGallery.innerHTML = '';
            
            // Sample images for demonstration
            const sampleImages = [
                {url: 'https://picsum.photos/200/300?nature', title: 'Nature'},
                {url: 'https://picsum.photos/200/300?tech', title: 'Technology'},
                {url: 'https://picsum.photos/200/300?city', title: 'City'},
                {url: 'https://picsum.photos/200/300?animal', title: 'Animals'}
            ];
            
            sampleImages.forEach(img => {
                const imgElement = document.createElement('div');
                imgElement.className = 'image-item';
                imgElement.innerHTML = `<img src="${img.url}" alt="${img.title}">`;
                imageGallery.appendChild(imgElement);
            });
        }

        document.getElementById('generate-image').addEventListener('click', () => {
            const prompt = document.getElementById('image-prompt').value;
            const style = document.getElementById('image-style').value;
            
            if (!prompt) {
                alert('Please enter a description for the image');
                return;
            }
            
            document.getElementById('image-spinner').style.display = 'block';
            
            // Simulate API call delay
            setTimeout(() => {
                document.getElementById('image-spinner').style.display = 'none';
                
                // Create a new image element
                const imageGallery = document.getElementById('image-gallery');
                const newImage = document.createElement('div');
                newImage.className = 'image-item';
                
                // Use a placeholder service for demo purposes
                // In a real implementation, this would be the AI-generated image
                const imageId = Math.floor(Math.random() * 1000);
                newImage.innerHTML = `
                    <img src="https://picsum.photos/200/300?random=${imageId}" alt="Generated image for: ${prompt}">
                    <div style="padding:10px; font-size:12px;">${prompt}</div>
                `;
                
                // Add to the beginning of the gallery
                imageGallery.insertBefore(newImage, imageGallery.firstChild);
                
                // Show success message
                const successMsg = document.createElement('div');
                successMsg.innerHTML = `<p style="color:green; margin:10px 0;">Image generated successfully!</p>`;
                document.getElementById('image-result').insertBefore(successMsg, imageGallery);
                
                // Remove the message after 3 seconds
                setTimeout(() => {
                    successMsg.remove();
                }, 3000);
            }, 2000);
        });

        // Translator
        document.getElementById('translate-btn').addEventListener('click', () => {
            const sourceLang = document.getElementById('source-lang').value;
            const targetLang = document.getElementById('target-lang').value;
            const text = document.getElementById('translate-text').value;
            
            if (!text) {
                alert('Please enter text to translate');
                return;
            }
            
            document.getElementById('translate-spinner').style.display = 'block';
            document.getElementById('translation-result').innerHTML = '';
            
            // Simulate API call delay
            setTimeout(() => {
                document.getElementById('translate-spinner').style.display = 'none';
                
                // Simulate translation
                const languages = {
                    'en': 'English',
                    'bn': 'Bengali',
                    'hi': 'Hindi',
                    'ar': 'Arabic',
                    'es': 'Spanish'
                };
                
                document.getElementById('translation-result').innerHTML = `
                    <p><strong>Translation (${languages[sourceLang]} to ${languages[targetLang]}):</strong></p>
                    <p>${text} - [Translated]</p>
                    <p><em>Note: This is a simulated translation. Actual translation would use LibreTranslate API.</em></p>
                `;
            }, 1500);
        });

        // AI Tools Hub
        document.getElementById('generate-ai').addEventListener('click', () => {
            const tool = document.getElementById('ai-tool-select').value;
            const input = document.getElementById('ai-input').value;
            
            if (!input) {
                alert('Please enter some input text');
                return;
            }
            
            document.getElementById('ai-spinner').style.display = 'block';
            document.getElementById('ai-result').innerHTML = '';
            
            // Simulate API call delay
            setTimeout(() => {
                document.getElementById('ai-spinner').style.display = 'none';
                
                // Generate sample output based on tool
                let output = '';
                
                switch(tool) {
                    case 'text-summarizer':
                        output = `<h3>Summary:</h3><p>This is a summarized version of your text containing the main points and key information.</p>`;
                        break;
                    case 'content-rewriter':
                        output = `<h3>Rewritten Content:</h3><p>This is a rewritten version of your text that maintains the original meaning but uses different phrasing and structure.</p>`;
                        break;
                    case 'code-generator':
                        output = `<h3>Generated Code:</h3><pre><code>function example() {\n  console.log("This is sample code generated based on your input");\n}</code></pre>`;
                        break;
                    case 'sentiment-analysis':
                        output = `<h3>Sentiment Analysis Result:</h3><p>The text appears to have a positive sentiment with a confidence score of 85%.</p>`;
                        break;
                }
                
                document.getElementById('ai-result').innerHTML = output;
            }, 1500);
        });
    </script>
</body>
</html>
