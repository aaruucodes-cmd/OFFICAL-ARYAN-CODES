
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ARYAN CODES - Professional Web Design, Development & Video Editing</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
font-family: system-ui, -apple-system, 'Segoe UI', Roboto, sans-serif;
            line-height: 1.6;
            color: #fff;
            background: linear-gradient(135deg, #0a0a0a 0%, #1a1a2e 50%, #16213e 100%);
            overflow-x: hidden;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        header {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(10,10,10,0.95);
            backdrop-filter: blur(10px);
            z-index: 1000;
            padding: 1rem 0;
        }
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            background: linear-gradient(45deg, #00ff88, #ff00ff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }
        .nav-links a {
            color: #fff;
            text-decoration: none;
            transition: color 0.3s;
        }
        .nav-links a:hover {
            color: #00ff88;
        }
        .hamburger {
            display: none;
            flex-direction: column;
            cursor: pointer;
        }
        .hamburger span {
            width: 25px;
            height: 3px;
            background: #fff;
            margin: 3px 0;
            transition: 0.3s;
        }
        section {
            padding: 100px 0;
            min-height: 100vh;
            display: flex;
            align-items: center;
        }
        h1 {
            font-size: clamp(3rem, 8vw, 6rem);
            font-weight: 700;
            margin-bottom: 1rem;
            background: linear-gradient(45deg, #00ff88, #ff00ff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        h2 {
            font-size: clamp(2rem, 5vw, 3.5rem);
            text-align: center;
            margin-bottom: 4rem;
            opacity: 0.9;
        }
        p {
            font-size: 1.2rem;
            max-width: 600px;
            margin: 0 auto 2rem;
            opacity: 0.8;
        }
        .btn {
            display: inline-block;
            padding: 15px 40px;
            background: linear-gradient(45deg, #00ff88, #00cc66);
            color: #000;
            text-decoration: none;
            border-radius: 50px;
            font-weight: 600;
            transition: all 0.3s;
            box-shadow: 0 10px 30px rgba(0,255,136,0.3);
        }
        .btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 40px rgba(0,255,136,0.5);
        }
        .btn-secondary {
            background: transparent;
            border: 2px solid #00ff88;
            color: #00ff88;
        }
        .btn-secondary:hover {
            background: #00ff88;
            color: #000;
        }
        .services-grid, .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 4rem;
        }
        .card {
            background: rgba(255,255,255,0.05);
            backdrop-filter: blur(20px);
            border-radius: 20px;
            padding: 2.5rem;
            text-align: center;
            transition: all 0.4s;
            border: 1px solid rgba(255,255,255,0.1);
        }
        .card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 60px rgba(0,255,136,0.2);
        }
        .card i {
            font-size: 4rem;
            background: linear-gradient(45deg, #00ff88, #ff00ff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 1rem;
        }
        .portfolio-item {
            position: relative;
            border-radius: 20px;
            overflow: hidden;
            height: 300px;
            background: linear-gradient(45deg, #667eea 0%, #764ba2 100%);
        }
        .portfolio-item::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(0,0,0,0.5);
            z-index: 1;
        }
        .portfolio-overlay {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            z-index: 2;
            text-align: center;
            color: #fff;
        }
        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 4rem;
        }
        .contact-item {
            text-align: center;
            padding: 2rem;
        }
        .whatsapp-btn {
            display: block;
            width: 200px;
            margin: 1rem auto;
            background: #25D366;
        }
        footer {
            background: rgba(0,0,0,0.8);
            text-align: center;
            padding: 2rem;
        }
        @media (max-width: 768px) {
            .hamburger {
                display: flex;
            }
            .nav-links {
                position: fixed;
                left: -100%;
                top: 70px;
                flex-direction: column;
                background-color: #0a0a0a;
                width: 100%;
                text-align: center;
                transition: 0.3s;
                padding: 2rem 0;
            }
            .nav-links.active {
                left: 0;
            }
            section {
                padding: 80px 0;
            }
        }
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        .fade-in {
            animation: fadeInUp 1s ease forwards;
        }
        .profile-photo {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            background: linear-gradient(45deg, #00ff88, #ff00ff);
            margin: 0 auto 2rem;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3rem;
            font-weight: 700;
            box-shadow: 0 10px 30px rgba(0,255,136,0.4);
            transition: all 0.3s;
        }
        .profile-photo:hover {
            transform: rotate(5deg) scale(1.05);
        }
    </style>
</head>
<body>
    <header>
        <nav class="container">
            <div class="logo">ARYAN CODES</div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#portfolio">Portfolio</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
            <div class="hamburger">
                <span></span>
                <span></span>
                <span></span>
            </div>
        </nav>
    </header>

    <section id="home" class="hero">
        <div class="container">
    <h1 class="fade-in">ARYAN CODES</h1>
            <div class="profile-photo fade-in">
                <span>AC</span>
            </div>
            <p class="fade-in">Transforming Ideas into Stunning Digital Experiences. Professional Web Design, Custom Website Development & High-Quality Video Editing Services.</p>
            <div>
                <a href="#contact" class="btn fade-in">Get Started</a>
                <a href="https://wa.me/917772075898" class="btn btn-secondary fade-in" style="margin-left: 1rem;">WhatsApp Now</a>
            </div>
        </div>
    </section>

    <section id="services">
        <div class="container">
            <h2>Our Services</h2>
            <div class="services-grid">
                <div class="card fade-in">
                    <i>🎨</i>
                    <h3>Web Design</h3>
                    <p>Modern, responsive designs tailored to your brand. Pixel-perfect UI/UX that captivates visitors.</p>
                </div>
                <div class="card fade-in">
                    <i>🌐</i>
                    <h3>Website Development</h3>
                    <p>Custom websites built with latest tech. Fast, secure, and scalable solutions for your business.</p>
                </div>
                <div class="card fade-in">
                    <i>🎥</i>
                    <h3>Video Editing</h3>
                    <p>Professional video editing for ads, promos, social media. Elevate your content to pro level.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="pricing">
        <div class="container">
            <h2>Transparent Pricing</h2>
            <p>Affordable packages for every need. Custom quotes available.</p>
            <div class="services-grid">
                <div class="card fade-in">
                    <h3>💎 Professional Website</h3>
                    <p>Advanced features, custom design, full functionality</p>
                    <strong>₹35,000 - ₹40,000</strong>
                </div>
                <div class="card fade-in">
                    <h3>⭐ Advance Websites </h3>
                    <p>Good quality, responsive, standard features</p>
                    <strong>₹25,000 - ₹30,000</strong>
                </div>
                <div class="card fade-in">
                    <h3>🔥 Basic Website</h3>
                    <p>Essential pages, clean design, fast delivery</p>
                    <strong>Starts at ₹15,000</strong>
                </div>
            </div>
            <div style="text-align: center; margin-top: 3rem;">
                <a href="#contact" class="btn">Get Custom Quote</a>
            </div>
        </div>
    </section>

    <section id="portfolio">
        <div class="container">
            <h2>Portfolio Highlights</h2>
            <p>Some of our recent projects showcasing modern design & functionality.</p>
            <div class="portfolio-grid">
                <div class="portfolio-item fade-in">
                    <div class="portfolio-overlay">
                        <h3>Hotels Site</h3>
                        <p>Luxury hotel template with booking system</p>
                    </div>
                </div>
                <div class="portfolio-item fade-in" style="background: linear-gradient(45deg, #ff6b6b, #feca57);">
                    <div class="portfolio-overlay">
                        <h3>E-Commerce Store</h3>
                        <p>Fully functional online shop</p>
                    </div>
                </div>
                <div class="portfolio-item fade-in" style="background: linear-gradient(45deg, #a8edea, #fed6e3);">
                    <div class="portfolio-overlay">
                        <h3>Portfolio Site</h3>
                        <p>Creative agency showcase</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="contact">
        <div class="container">
            <h2>Ready to Start Your Project?</h2>
            <p>Get in touch today for a free consultation. Let's build something amazing together!</p>
            <div class="contact-grid">
                <div class="contact-item fade-in">
                    <h3>📱 WhatsApp Business</h3>
                    <p>Message ARYAN CODES directly</p>
                    <a href="https://wa.me/917772075898" class="btn whatsapp-btn" target="_blank">Chat on WhatsApp</a>
                </div>
                <div class="contact-item fade-in">
                    <h3>📸 Instagram</h3>
                    <p>Follow for updates & inspiration</p>
                    <a href="https://www.instagram.com/aaruu_codes?igsh=Z3RoOGhoNjE0bHJr" class="btn btn-secondary" target="_blank">Follow @aaruu_codes</a>
                </div>
                <div class="contact-item fade-in">
                    <h3>✉️ Business Email</h3>
                    <p>aryanjaiswalji25@gmail.com</p>
                    <a href="mailto:aryanjaiswalji25@gmail.com" class="btn btn-secondary" target="_blank">Send Email</a>
                </div>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <p>&copy; 2024 ARYAN CODES. All rights reserved. | Professional Web & Video Editing</p>
        </div>
    </footer>

    <script>
        // Smooth scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Mobile menu toggle
        const hamburger = document.querySelector('.hamburger');
        const navLinks = document.querySelector('.nav-links');
        hamburger.addEventListener('click', () => {
            navLinks.classList.toggle('active');
        });

        // Fade in on scroll
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('fade-in');
                }
            });
        });
        document.querySelectorAll('.fade-in').forEach(el => observer.observe(el));
    </script>

