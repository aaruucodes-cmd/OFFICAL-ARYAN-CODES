<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ARYAN CODES - FIXED PERFECT SALE</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        html, body { height: 100%; overflow-x: hidden; }
        body { font-family: system-ui, sans-serif; line-height: 1.6; color: #fff; background: linear-gradient(135deg, #0a0a0a 0%, #1a1a2e 50%, #16213e 100%); }
        .container { max-width: 1200px; margin: 0 auto; padding: 0 clamp(12px, 4vw, 24px); width: 100%; position: relative; }
        .preloader { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: linear-gradient(135deg, #0a0a0a 0%, #1a1a2e 50%, #16213e 100%); display: flex; flex-direction: column; align-items: center; justify-content: center; z-index: 9999; transition: all .6s ease; }
        .preloader.hidden { opacity: 0; transform: scale(0.9); visibility: hidden; }
        .logo-spin { font-size: clamp(3rem, 10vw, 6rem); font-weight: 700; background: linear-gradient(45deg, #00ff88, #ff00ff); -webkit-background-clip: text; -webkit-text-fill-color: transparent; animation: spin 1.5s linear infinite; }
        @keyframes spin { from { transform: rotate(0deg); } to { transform: rotate(360deg); } }
        .sale-live { position: fixed; top: 0; left: 0; right: 0; background: linear-gradient(90deg, #ff0000, #ff4444, #ff0000); color: #fff; text-align: center; padding: clamp(0.8rem, 2.5vw, 1.2rem); font-size: clamp(1.1rem, 3.5vw, 1.4rem); z-index: 1000; font-weight: 800; animation: pulse 1.5s infinite; box-shadow: 0 4px 20px rgba(255,0,0,0.5); }
        .sale-live .countdown { font-size: clamp(1.2rem, 4vw, 1.6rem); margin-top: 0.3rem; }
        .sale-live .countdown span { background: #000; color: #00ff88; padding: clamp(0.4rem, 1.8vw, 0.6rem) clamp(0.6rem, 2.2vw, 1rem); border-radius: 12px; margin: 0 0.3rem; font-weight: 700; box-shadow: 0 2px 10px rgba(0,255,136,0.3); }
        @keyframes pulse { 0%, 100% { opacity: 1; transform: scale(1); } 50% { opacity: 0.95; transform: scale(1.02); } }
        header { position: fixed; top: 0; width: 100%; background: rgba(10,10,10,0.97); backdrop-filter: blur(15px); z-index: 999; padding: clamp(1rem, 2.5vw, 1.5rem) 0; border-bottom: 1px solid rgba(255,255,255,0.1); }
        nav { display: flex; justify-content: space-between; align-items: center; }
        .logo { font-size: clamp(1.6rem, 4.5vw, 2.1rem); font-weight: 800; background: linear-gradient(45deg, #00ff88, #ff00ff); -webkit-background-clip: text; -webkit-text-fill-color: transparent; }
        .nav-links { display: flex; list-style: none; gap: clamp(1.5rem, 4vw, 2.5rem); }
        .nav-links a { color: #fff; text-decoration: none; font-weight: 600; transition: all 0.3s; font-size: clamp(1rem, 2.8vw, 1.1rem); position: relative; }
        .nav-links a:hover { color: #00ff88; }
        .nav-links a::after { content: ''; position: absolute; width: 0; height: 2px; bottom: -4px; left: 50%; background: #00ff88; transition: all 0.3s; }
        .nav-links a:hover::after { width: 100%; left: 0; }
        .hamburger { display: none; flex-direction: column; cursor: pointer; gap: 4px; }
        .hamburger span { width: 28px; height: 3px; background: #fff; transition: all 0.3s; border-radius: 2px; }
        .insta-icon { position: fixed; bottom: clamp(20px, 5vw, 30px); right: clamp(20px, 5vw, 30px); width: clamp(56px, 16vw, 65px); height: clamp(56px, 16vw, 65px); background: linear-gradient(45deg, #f09433 0%, #e6683c 25%, #dc2743 50%, #cc2366 75%, #bc1888 100%); border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: clamp(1.8rem, 7vw, 2.3rem); cursor: pointer; box-shadow: 0 10px 30px rgba(244,148,51,0.5); transition: all 0.4s; z-index: 500; color: #fff; text-decoration: none; border: 2px solid rgba(255,255,255,0.2); }
        .insta-icon:hover { transform: scale(1.15) rotate(5deg); box-shadow: 0 15px 45px rgba(244,148,51,0.7); }
        section { padding: clamp(130px, 24vh, 160px) 0 clamp(100px, 20vh, 130px); min-height: 100vh; display: flex; flex-direction: column; align-items: center; justify-content: center; width: 100%; }
        h1 { font-size: clamp(3rem, 11vw, 7rem); font-weight: 900; margin-bottom: clamp(1.5rem, 6vw, 2.5rem); background: linear-gradient(45deg, #00ff88 0%, #ff00ff 50%, #00ff88 100%); -webkit-background-clip: text; -webkit-text-fill-color: transparent; text-align: center; letter-spacing: -0.02em; text-shadow: 0 0 40px rgba(0,255,136,0.3); }
        h2 { font-size: clamp(2.2rem, 7vw, 4rem); text-align: center; margin-bottom: clamp(2.5rem, 12vw, 5rem); opacity: 0.95; font-weight: 700; letter-spacing: -0.01em; }
        p { font-size: clamp(1.1rem, 3.5vw, 1.4rem); max-width: 650px; margin: 0 auto clamp(1.5rem, 5vw, 3rem); text-align: center; opacity: 0.92; line-height: 1.7; }
        .profile-photo { width: clamp(140px, 32vw, 170px); height: clamp(140px, 32vw, 170px); border-radius: 50%; background: linear-gradient(135deg, #00ff88 0%, #ff00ff 100%); margin: clamp(1.5rem, 6vw, 3rem) auto; display: flex; align-items: center; justify-content: center; font-size: clamp(2.5rem, 9vw, 4rem); font-weight: 900; box-shadow: 0 20px 60px rgba(0,255,136,0.5); transition: all 0.4s; animation: floatPulse 4s ease-in-out infinite; border: 3px solid rgba(255,255,255,0.2); backdrop-filter: blur(10px); }
        @keyframes floatPulse { 0%, 100% { transform: translateY(0) scale(1); box-shadow: 0 20px 60px rgba(0,255,136,0.5); } 50% { transform: translateY(-15px) scale(1.05); box-shadow: 0 35px 80px rgba(0,255,136,0.7); } }
        .btn { display: inline-flex; align-items: center; gap: 0.8rem; padding: clamp(14px, 4vw, 18px) clamp(35px, 9vw, 50px); background: linear-gradient(135deg, #00ff88 0%, #00cc66 100%); color: #000; text-decoration: none; border-radius: 60px; font-weight: 700; transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1); box-shadow: 0 15px 40px rgba(0,255,136,0.4); margin: 0 clamp(1rem, 3vw, 1.5rem); font-size: clamp(1.1rem, 3vw, 1.3rem); position: relative; overflow: hidden; }
        .btn::before { content: ''; position: absolute; top: 0; left: -100%; width: 100%; height: 100%; background: linear-gradient(90deg, transparent, rgba(255,255,255,0.3), transparent); transition: left 0.5s; }
        .btn:hover { transform: translateY(-8px) scale(1.05); box-shadow: 0 25px 60px rgba(0,255,136,0.6); }
        .btn:hover::before { left: 100%; }
        .whatsapp-btn { background: linear-gradient(135deg, #25D366 0%, #128C7E 100%); color: #fff !important; box-shadow: 0 15px 40px rgba(37,211,102,0.4); }
        .whatsapp-btn:hover { box-shadow: 0 25px 60px rgba(37,211,102,0.6); }
        .portfolio-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(clamp(280px, 26vw, 320px), 1fr)); gap: clamp(2rem, 6vw, 3rem); margin-top: clamp(2rem, 8vw, 4rem); width: 100%; }
        .portfolio-item { position: relative; border-radius: 25px; overflow: hidden; height: clamp(320px, 42vh, 380px); cursor: pointer; transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1); aspect-ratio: 4/3; }
        .portfolio-item::before { content: ''; position: absolute; inset: 0; background: rgba(0,0,0,0.4); z-index: 1; transition: all 0.3s; }
        .portfolio-item:hover { transform: translateY(-15px) scale(1.03); box-shadow: 0 30px 80px rgba(0,0,0,0.5); }
        .portfolio-overlay { position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); z-index: 2; text-align: center; color: #fff; width: 92%; background: rgba(0,0,0,0.8); backdrop-filter: blur(15px); padding: clamp(1.5rem, 4vw, 2rem); border-radius: 20px; font-size: clamp(1rem, 2.8vw, 1.2rem); transition: all 0.3s; }
        .portfolio-overlay h3 { font-size: clamp(1.4rem, 4vw, 1.8rem); margin-bottom: 0.8rem; font-weight: 700; }
        .sale-badge { position: absolute; top: clamp(15px, 4vw, 20px); left: clamp(15px, 4vw, 20px); background: linear-gradient(135deg, #ff4444, #ff6666); color: #fff; padding: clamp(0.7rem, 2vw, 1rem) clamp(1rem, 3vw, 1.5rem); border-radius: 30px; font-weight: 800; font-size: clamp(1rem, 3vw, 1.2rem); z-index: 3; box-shadow: 0 8px 25px rgba(255,68,68,0.6); border: 2px solid rgba(255,255,255,0.2); }
        .old-price { display: block; font-size: clamp(0.8rem, 2.5vw, 1rem); opacity: 0.85; text-decoration: line-through; margin-top: 0.3rem; }
        .contact-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(clamp(260px, 28vw, 300px), 1fr)); gap: clamp(2rem, 6vw, 3rem); margin-top: clamp(3rem, 10vw, 5rem); width: 100%; }
        .contact-item { text-align: center; padding: clamp(2.5rem, 8vw, 3.5rem); background: rgba(255,255,255,0.08); backdrop-filter: blur(20px); border-radius: 25px; border: 1px solid rgba(255,255,255,0.15); transition: all 0.3s; width: 100%; }
        .contact-item:hover { transform: translateY(-10px); background: rgba(255,255,255,0.12); box-shadow: 0 20px 60px rgba(0,0,0,0.4); }
        .insta-promo { margin-top: clamp(2rem, 6vw, 4rem); text-align: center; background: linear-gradient(135deg, #f09433, #e6683c); -webkit-background-clip: text; -webkit-text-fill-color: transparent; font-size: clamp(1.3rem, 4vw, 1.8rem); font-weight: 700; animation: shimmer 2s infinite; }
        @keyframes shimmer { 0% { background-position: 0%; } 100% { background-position: 200%; } }
        @media (max-width: 1024px) { .portfolio-grid { grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 2rem; } }
        @media (max-width: 768px) { .hamburger { display: flex; } .nav-links { position: fixed; left: -100%; top: 70px; flex-direction: column; background: rgba(10,10,10,0.98); width: 100%; transition: left 0.4s; padding: clamp(2rem, 8vw, 3rem) 0; text-align: center; z-index: 998; border-bottom: 1px solid rgba(255,255,255,0.1); backdrop-filter: blur(20px); } .nav-links.active { left: 0; } .portfolio-grid { grid-template-columns: 1fr; } .btn { display: block; margin: clamp(1rem, 4vw, 1.5rem) auto !important; } .sale-live { padding: clamp(0.9rem, 3vw, 1.3rem); font-size: clamp(1.2rem, 4vw, 1.5rem); } }
        @media (max-width: 480px) { section { padding: clamp(110px, 26vh, 140px) 0 clamp(90px, 22vh, 120px); } .container { padding: 0 clamp(10px, 5vw, 18px); } }
        @media (max-width: 360px) { section { padding: clamp(100px, 24vh, 130px) 0 clamp(80px, 20vh, 110px); } .portfolio-item { height: clamp(260px, 48vh, 300px); } .sale-live { padding: clamp(1rem, 3.5vw, 1.4rem); } }
        @keyframes fadeInUp { from { opacity: 0; transform: translateY(50px); } to { opacity: 1; transform: translateY(0); } }
        .fade-in { opacity: 0; animation: fadeInUp 1s ease-out forwards; }
        body { opacity: 0; animation: fadeBody 0.8s forwards 2.5s; }
        @keyframes fadeBody { to { opacity: 1; } }
    </style>
</head>
<body>
    <!-- PRELOADER -->
    <div class="preloader" id="preloader">
        <div class="logo-spin">ARYAN CODES</div>
    </div>

    <!-- LIVE SALE BANNER -->
    <div class="sale-live" id="saleBanner">
        <h3>🔴 LIVE SALE! ⏱️ Limited Time</h3>
        <div class="countdown" id="countdown"></div>
    </div>

    <!-- HEADER -->
    <header>
        <nav class="container">
            <div class="logo">ARYAN CODES</div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#portfolio">Portfolio</a></li>
                <li><a href="#contact">Buy Now</a></li>
            </ul>
            <div class="hamburger">
                <span></span><span></span><span></span>
            </div>
        </nav>
    </header>

    <!-- INSTAGRAM ICON -->
    <a href="https://instagram.com/aaruu_codes" class="insta-icon" target="_blank" title="DM @aaruu_codes for orders">📸</a>

    <!-- HERO -->
    <section id="home">
        <div class="container">
            <h1 class="fade-in">ARYAN CODES LIVE SALE!</h1>
            <div class="profile-photo fade-in">AC</div>
            <p class="fade-in">Perfect Responsive Templates & Custom Sites<br><strong>Anniversary • Birthday • Proposal • Hotels • Shops</strong></p>
            <div class="fade-in">
                <a href="#portfolio" class="btn">View Templates 🔥</a>
                <a href="https://wa.me/917772075898?text=Hi Aryan! LIVE SALE order [Template/Hotel]" class="whatsapp-btn">Buy Now 📱</a>
            </div>
        </div>
    </section>

    <!-- PORTFOLIO -->
    <section id="portfolio">
        <div class="container">
            <h2 class="fade-in">Templates & Custom Sites</h2>
            <p class="fade-in">Click to preview templates • DM for custom • <strong>LIVE SALE prices for 10 days only</strong></p>
            <div class="portfolio-grid">
                <div class="portfolio-item fade-in" onclick="window.open('templates/anniversary.html', '_blank')">
                    <div class="sale-badge">₹149<br><span class="old-price">was ₹799</span></div>
                    <div class="portfolio-overlay">
                        <h3>💕 Anniversary Template</h3>
                        <p>Timeline + Music + Responsive</p>
                    </div>
                </div>
                <div class="portfolio-item fade-in" onclick="window.open('templates/birthday-festival.html', '_blank')">
                    <div class="sale-badge">₹199<br><span class="old-price">was ₹999</span></div>
                    <div class="portfolio-overlay">
                        <h3>🎂 Birthday Festival</h3>
                        <p>Diwali/Holi Fireworks + Custom</p>
                    </div>
                </div>
                <div class="portfolio-item fade-in" onclick="window.open('templates/love-proposal.html', '_blank')">
                    <div class="sale-badge">₹249<br><span class="old-price">was ₹1499</span></div>
                    <div class="portfolio-overlay">
                        <h3>💍 Love Proposal</h3>
                        <p>Interactive + Confetti + Typing</p>
                    </div>
                </div>
                <div class="portfolio-item fade-in">
                    <div class="sale-badge">₹999<br><span class="old-price">was ₹5000</span></div>
                    <div class="portfolio-overlay">
                        <h3>🏨 Hotel/Restaurant Site</h3>
                        <p>Custom Professional Responsive</p>
                    </div>
                </div>
                <div class="portfolio-item fade-in">
                    <div class="sale-badge">₹1999<br><span class="old-price">was ₹10000</span></div>
                    <div class="portfolio-overlay">
                        <h3>📱 Mobile Shop</h3>
                        <p>E-commerce Catalog + Booking</p>
                    </div>
                </div>
            </div>
            <div style="text-align: center; margin-top: clamp(4rem, 12vw, 6rem);">
                <a href="https://wa.me/917772075898?text=Hi Aryan! LIVE SALE - Need [anniversary/birthday/proposal/hotel/shop] website. Price?" class="btn whatsapp-btn" style="font-size: clamp(1.4rem, 4vw, 1.8rem); padding: clamp(20px, 5vw, 25px) clamp(60px, 12vw, 80px); box-shadow: 0 20px 50px rgba(37,211,102,0.5);">
                    📱 INSTANT ORDER WhatsApp <span style="font-size: 0.9em;">(10% EXTRA OFF)</span>
                </a>
            </div>
        </div>
    </section>

    <!-- CONTACT -->
    <section id="contact">
        <div class="container">
            <h2 class="fade-in">Buy LIVE</h2>
            <p class="fade-in">Instant response • Custom quotes • 24h delivery</p>
            <div class="contact-grid">
                <div class="contact-item fade-in">
                    <h3>📱 WhatsApp Live Orders</h3>
                    <p>Get quote & instant delivery</p>
                    <a href="https://wa.me/917772075898?text=Live sale website order!" class="btn whatsapp-btn">Order ₹149→</a>
                </div>
                <div class="contact-item fade-in">
                    <h3>📸 Instagram Demos</h3>
                    <p>Live previews & support</p>
                    <a href="https://instagram.com/aaruu_codes" class="btn" target="_blank">DM @aaruu_codes</a>
                </div>
            </div>
            <div class="insta-promo fade-in">
                Follow @aaruu_codes for LIVE updates & extra offers!
            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer style="background: rgba(0,0,0,0.9); text-align: center; padding: clamp(2.5rem, 8vw, 4rem); border-top: 1px solid rgba(255,255,255,0.1); font-size: clamp(0.95rem, 2.8vw, 1.1rem);">
        <p>&copy; 2025 ARYAN CODES | <strong>LIVE SALE 10 Days Only</strong> | All Sites 100% Responsive | <a href="#portfolio" style="color: #00ff88; text-decoration: none;">↑ Portfolio</a></p>
    </footer>

    <script>
        // Preloader + Staggered Animations
        window.addEventListener('load', () => {
            setTimeout(() => {
                document.getElementById('preloader').classList.add('hidden');
            }, 2200);
            document.querySelectorAll('.fade-in').forEach((el, i) => {
                el.style.animationDelay = `${Math.min(i * 0.18, 1)}s`;
            });
        });

        // LIVE SALE Countdown (10 days, localStorage, auto-off)
        let saleEnd = parseInt(localStorage.getItem('saleEnd')) || (Date.now() + 10 * 24 * 60 * 60 * 1000);
        function updateLiveSale() {
            let distance = saleEnd - Date.now();
            let banner = document.getElementById('saleBanner');
            let countdown = document.getElementById('countdown');
            if (distance < 0) {
                banner.innerHTML = '<h3 style="animation: none;">🔴 SALE ENDED - Regular Prices</h3>';
                countdown.remove();
                return;
            }
            let days = Math.floor(distance / (1000 * 60 * 60 * 24));
            let hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            let minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
            let seconds = Math.floor((distance % (1000 * 60)) / 1000);
            countdown.innerHTML = `<span>${days}d</span><span>${hours}h</span><span>${minutes}m</span><span>${seconds}s</span>`;
        }
        setInterval(updateLiveSale, 1000);
        updateLiveSale();
        localStorage.setItem('saleEnd', saleEnd);

        // Mobile Menu
        document.querySelector('.hamburger').onclick = () => {
            document.querySelector('.nav-links').classList.toggle('active');
        };

        // Smooth Scroll
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth',
                    block: 'start'
                });
            });
        });
    </script>
</body>
</html>

