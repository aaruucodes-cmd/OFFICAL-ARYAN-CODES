<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ARYAN CODES - Template SALE! Professional Web Design</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { 
            font-family: system-ui, sans-serif; 
            line-height: 1.6; 
            color: #fff; 
            background: linear-gradient(135deg, #0a0a0a 0%, #1a1a2e 50%, #16213e 100%);
            overflow-x: hidden; 
        }
        .container { max-width: 1200px; margin: 0 auto; padding: 0 20px; }
        /* Sale Banner */
        .sale-banner {
            background: linear-gradient(45deg, #ff0000, #ff4444);
            color: #fff;
            text-align: center;
            padding: 1rem;
            position: relative;
            z-index: 100;
        }
        .countdown { font-size: 1.5rem; font-weight: bold; margin: 0.5rem 0; }
        .countdown span { background: #000; padding: 0.5rem 1rem; border-radius: 10px; margin: 0 0.2rem; }
        .expired { opacity: 0.5; }
        /* Header */
        header { position: fixed; top: 0; width: 100%; background: rgba(10,10,10,0.95); backdrop-filter: blur(10px); z-index: 99; padding: 1rem 0; }
        nav { display: flex; justify-content: space-between; align-items: center; }
        .logo { font-size: 1.8rem; font-weight: 700; background: linear-gradient(45deg, #00ff88, #ff00ff); -webkit-background-clip: text; -webkit-text-fill-color: transparent; }
        .nav-links { display: flex; list-style: none; gap: 2rem; }
        .nav-links a { color: #fff; text-decoration: none; transition: color 0.3s; }
        .nav-links a:hover { color: #00ff88; }
        /* Hero */
        #home { padding: 120px 0; min-height: 100vh; display: flex; align-items: center; }
        h1 { font-size: clamp(3rem, 8vw, 6rem); font-weight: 700; margin-bottom: 1rem; background: linear-gradient(45deg, #00ff88, #ff00ff); -webkit-background-clip: text; -webkit-text-fill-color: transparent; }
        .profile-photo { width: 150px; height: 150px; border-radius: 50%; background: linear-gradient(45deg, #00ff88, #ff00ff); margin: 2rem auto; display: flex; align-items: center; justify-content: center; font-size: 3rem; font-weight: 700; box-shadow: 0 10px 30px rgba(0,255,136,0.4); transition: all 0.3s; }
        /* Portfolio */
        #portfolio { padding: 100px 0; }
        h2 { font-size: clamp(2rem, 5vw, 3.5rem); text-align: center; margin-bottom: 4rem; opacity: 0.9; }
        .portfolio-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 2rem; }
        .portfolio-item { position: relative; border-radius: 20px; overflow: hidden; height: 350px; cursor: pointer; transition: transform 0.3s; }
        .portfolio-item:hover { transform: scale(1.05); }
        .portfolio-overlay { position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); z-index: 2; text-align: center; color: #fff; width: 90%; }
        /* Sale Badge */
        .sale-badge { position: absolute; top: 10px; right: 10px; background: #ff4444; color: #fff; padding: 0.5rem 1rem; border-radius: 20px; font-weight: bold; font-size: 1rem; z-index: 3; box-shadow: 0 4px 12px rgba(255,68,68,0.4); }
        .old-price { text-decoration: line-through; opacity: 0.7; font-size: 0.9rem; margin-left: 0.5rem; }
        /* Buttons */
        .btn { display: inline-block; padding: 15px 40px; background: linear-gradient(45deg, #00ff88, #00cc66); color: #000; text-decoration: none; border-radius: 50px; font-weight: 600; transition: all 0.3s; box-shadow: 0 10px 30px rgba(0,255,136,0.3); }
        .btn:hover { transform: translateY(-5px); box-shadow: 0 15px 40px rgba(0,255,136,0.5); }
        .whatsapp-btn { background: #25D366; color: #fff !important; }
        /* Responsive */
        @media (max-width: 768px) { .portfolio-grid { grid-template-columns: 1fr; } }
        @media (max-width: 480px) { .container { padding: 0 15px; } section { padding: 80px 0; } }
    </style>
</head>
<body>
    <div class="sale-banner" id="saleBanner">
        <h3>🔥 LIMITED FLASH SALE! Template Websites 70% OFF - <span class="countdown" id="countdown"></span></h3>
        <p>Grab now before prices go up! Valid for 10 days only.</p>
    </div>

    <header>
        <nav class="container">
            <div class="logo">ARYAN CODES</div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#portfolio">Templates</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section id="home">
        <div class="container">
            <h1>Template SALE! 💥</h1>
            <div class="profile-photo">AC</div>
            <p>Premium Animated Templates at UNBEATABLE Prices! Perfect for Anniversary, Birthday, Festivals & Proposals. Fully Responsive, Customizable HTML.</p>
            <a href="#portfolio" class="btn">See Templates</a>
            <a href="https://wa.me/917772075898" class="btn whatsapp-btn">Buy Now on WhatsApp</a>
        </div>
    </section>

    <section id="portfolio">
        <div class="container">
            <h2>Limited Time Templates - FLASH SALE!</h2>
            <div class="portfolio-grid">
                <div class="portfolio-item" style="background: linear-gradient(45deg, #ee7752, #e73c7e);" onclick="window.open('templates/anniversary.html', '_blank')">
                    <div class="sale-badge">₹199 <span class="old-price">₹799</span></div>
                    <div class="portfolio-overlay">
                        <h3>💕 Anniversary Template</h3>
                        <p>Romantic timeline, music, floating effects. Perfect celebration page!</p>
                    </div>
                </div>
                <div class="portfolio-item" style="background: linear-gradient(45deg, #f093fb, #fa709a);" onclick="window.open('templates/birthday-festival.html', '_blank')">
                    <div class="sale-badge">₹299 <span class="old-price">₹999</span></div>
                    <div class="portfolio-overlay">
                        <h3>🎂 Birthday / Festival</h3>
                        <p>Diwali, Holi, Birthday - Fireworks, custom wishes, cake animation!</p>
                    </div>
                </div>
                <div class="portfolio-item" style="background: linear-gradient(45deg, #667eea, #764ba2);" onclick="window.open('templates/love-proposal.html', '_blank')">
                    <div class="sale-badge">₹499 <span class="old-price">₹999</span></div>
                    <div class="portfolio-overlay">
                        <h3>💍 Love Proposal</h3>
                        <p>Typing message, heartbeat, confetti explosion - Yes/No modals!</p>
                    </div>
                </div>
            </div>
            <div style="text-align: center; margin-top: 4rem;">
                <a href="https://wa.me/917772075898?text=Hi! I want to buy the %20template" class="btn whatsapp-btn" style="font-size: 1.5rem; padding: 20px 60px;">BUY NOW - WhatsApp 🛒</a>
            </div>
        </div>
    </section>

    <section id="contact">
        <div class="container">
            <h2>Ready to Grab Your Template?</h2>
            <p>Instant delivery via WhatsApp. Customize & launch in minutes!</p>
            <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 2rem; margin-top: 3rem;">
                <div style="text-align: center;">
                    <h3>📱 WhatsApp</h3>
                    <a href="https://wa.me/917772075898" class="btn whatsapp-btn">Message Now</a>
                </div>
                <div style="text-align: center;">
                    <h3>✉️ Email</h3>
                    <p>aryanjaiswalji25@gmail.com</p>
                </div>
            </div>
        </div>
    </section>

    <footer style="background: rgba(0,0,0,0.8); text-align: center; padding: 2rem;">
        <p>&copy; 2025 ARYAN CODES | Limited Sale - Only 10 Days! | <a href="#portfolio" style="color: #00ff88;">Templates ↑</a></p>
    </footer>

    <script>
        // 10-Day Countdown
        function updateCountdown() {
            const saleEnd = localStorage.getItem('saleEnd');
            let endTime = saleEnd ? new Date(parseInt(saleEnd)) : new Date(Date.now() + 10 * 24 * 60 * 60 * 1000); // 10 days from now
            localStorage.setItem('saleEnd', endTime.getTime());
            
            const now = new Date().getTime();
            const distance = endTime - now;
            
            if (distance < 0) {
                document.getElementById('saleBanner').innerHTML = '<h3>Sale Ended! Regular prices now apply.</h3>';
                document.getElementById('saleBanner').classList.add('expired');
                return;
            }
            
            const days = Math.floor(distance / (1000 * 60 * 60 * 24));
            const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((distance % (1000 * 60)) / 1000);
            
            document.getElementById('countdown').innerHTML = `${days}d <span>${hours}h</span> <span>${minutes}m</span> <span>${seconds}s</span>`;
        }
        setInterval(updateCountdown, 1000);
        updateCountdown();

        // Smooth scroll
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({ behavior: 'smooth' });
            });
        });
    </script>
</body>
</html>
