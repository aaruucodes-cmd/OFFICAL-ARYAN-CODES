 <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ARYAN CODES - Professional Web Templates | Flash Sale</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        html, body { height: 100%; overflow-x: hidden; }
        body { font-family: system-ui, sans-serif; line-height: 1.6; color: #fff; background: linear-gradient(135deg, #0a0a0a 0%, #1a1a2e 50%, #16213e 100%); }
        .container { max-width: 1200px; margin: 0 auto; padding: 0 clamp(12px, 4vw, 24px); width: 100%; }
        /* Preloader Start Animation */
        .preloader { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: linear-gradient(135deg, #0a0a0a, #1a1a2e); display: flex; flex-direction: column; align-items: center; justify-content: center; z-index: 9999; transition: all .8s cubic-bezier(0.25, 0.46, 0.45, 0.94); }
        .preloader.hidden { opacity: 0; transform: scale(0.95); visibility: hidden; }
        .logo-spin { font-size: clamp(3rem, 12vw, 7rem); font-weight: 900; background: linear-gradient(45deg, #00ff88, #ff00ff, #00ff88); -webkit-background-clip: text; -webkit-text-fill-color: transparent; animation: spinGlow 2s linear infinite; }
        @keyframes spinGlow { 0% { transform: rotate(0deg) scale(1); filter: drop-shadow(0 0 20px #00ff88); } 50% { filter: drop-shadow(0 0 40px #ff00ff); } 100% { transform: rotate(360deg) scale(1); filter: drop-shadow(0 0 20px #00ff88); } }
        .load-bar { width: 200px; height: 4px; background: rgba(255,255,255,0.2); border-radius: 2px; overflow: hidden; margin-top: 2rem; }
        .load-progress { height: 100%; background: linear-gradient(90deg, #00ff88, #ff00ff); border-radius: 2px; width: 0%; animation: load 2s ease-out forwards; }
        @keyframes load { to { width: 100%; } }
        /* Sale Banner */
        .sale-live { position: fixed; top: 0; left: 0; right: 0; background: linear-gradient(90deg, #ff1744, #ff5722); color: #fff; text-align: center; padding: clamp(1rem, 3vw, 1.2rem); font-weight: 800; z-index: 1000; animation: slideDown 0.5s ease-out; box-shadow: 0 4px 20px rgba(255,23,68,0.4); }
        @keyframes slideDown { from { transform: translateY(-100%); } to { transform: translateY(0); } }
        .countdown { font-size: clamp(1.2rem, 4vw, 1.6rem); margin-top: 0.5rem; }
        .countdown span { background: rgba(0,0,0,0.8); padding: 0.5rem 1rem; border-radius: 20px; margin: 0 0.25rem; box-shadow: 0 4px 15px rgba(0,0,0,0.3); }
        /* Header */
        header { position: fixed; top: 0; width: 100%; background: rgba(10,10,10,0.95); backdrop-filter: blur(20px); z-index: 999; padding: clamp(1rem, 2.5vw, 1.4rem) 0; border-bottom: 1px solid rgba(255,255,255,0.1); }
        nav { display: flex; justify-content: space-between; align-items: center; }
        .logo { font-size: clamp(1.7rem, 5vw, 2.2rem); font-weight: 800; background: linear-gradient(45deg, #00ff88, #ff00ff); -webkit-background-clip: text; -webkit-text-fill-color: transparent; }
        .nav-links { display: flex; gap: 2.5rem; list-style: none; }
        .nav-links a { color: #fff; text-decoration: none; font-weight: 600; position: relative; transition: color 0.3s; }
        .nav-links a::after { content: ''; position: absolute; bottom: -5px; left: 0; width: 0; height: 2px; background: #00ff88; transition: width 0.3s; }
        .nav-links a:hover::after { width: 100%; }
        .nav-links a:hover { color: #00ff88; }
        .hamburger { display: none; flex-direction: column; gap: 5px; cursor: pointer; }
        .hamburger span { width: 30px; height: 3px; background: #fff; border-radius: 2px; transition: 0.3s; }
        /* Floating Instagram */
        .insta-fab { position: fixed; bottom: 25px; right: 25px; width: 70px; height: 70px; background: linear-gradient(45deg, #f09433, #e6683c, #dc2743); border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 2.2rem; box-shadow: 0 10px 30px rgba(244,148,51,0.5); transition: all 0.4s; z-index: 100; text-decoration: none; border: 3px solid rgba(255,255,255,0.3); }
        .insta-fab:hover { transform: scale(1.1) rotate(360deg); box-shadow: 0 20px 50px rgba(244,148,51,0.7); }
        /* Sections */
        section { padding: clamp(140px, 28vh, 170px) 0 clamp(110px, 22vh, 140px); display: flex; flex-direction: column; align-items: center; justify-content: center; }
        h1 { font-size: clamp(3.5rem, 12vw, 8rem); font-weight: 900; background: linear-gradient(45deg, #00ff88, #ff00ff); -webkit-background-clip: text; -webkit-text-fill-color: transparent; text-align: center; margin-bottom: 1.5rem; }
        h2 { font-size: clamp(2.5rem, 8vw, 4.5rem); text-align: center; margin-bottom: 3rem; opacity: 0.95; }
        p { font-size: clamp(1.1rem, 3.5vw, 1.4rem); text-align: center; max-width: 700px; margin-bottom: 2.5rem; opacity: 0.9; }
        .profile-img { width: clamp(160px, 35vw, 200px); height: clamp(160px, 35vw, 200px); border-radius: 50%; background: linear-gradient(135deg, #00ff88, #ff00ff); display: flex; align-items: center; justify-content: center; font-size: clamp(3rem, 10vw, 4.5rem); font-weight: 900; box-shadow: 0 25px 70px rgba(0,255,136,0.6); animation: pulseFloat 4s ease-in-out infinite; margin: 2rem auto; }
        @keyframes pulseFloat { 0%,100% { transform: translateY(0); } 50% { transform: translateY(-20px); } }
        .btn { padding: clamp(16px, 4.5vw, 20px) clamp(40px, 10vw, 60px); background: linear-gradient(135deg, #00ff88, #00cc66); color: #000; text-decoration: none; border-radius: 50px; font-weight: 700; font-size: clamp(1.1rem, 3vw, 1.3rem); transition: all 0.4s; box-shadow: 0 15px 40px rgba(0,255,136,0.4); display: inline-flex; align-items: center; gap: 1rem; margin: 0 1rem 1rem 0; }
        .btn:hover { transform: translateY(-8px); box-shadow: 0 25px 60px rgba(0,255,136,0.6); }
        .whatsapp-btn { background: linear-gradient(135deg, #25d366, #128c7e); color: #fff !important; box-shadow: 0 15px 40px rgba(37,211,102,0.5); }
        .insta-btn { background: linear-gradient(45deg, #f09433, #e6683c); color: #fff !important; box-shadow: 0 15px 40px rgba(244,148,51,0.5); }
        /* Portfolio */
        .portfolio-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(clamp(300px, 28vw, 350px), 1fr)); gap: 2.5rem; width: 100%; }
        .portfolio-item { position: relative; border-radius: 25px; height: clamp(340px, 45vh, 400px); cursor: pointer; transition: all 0.5s cubic-bezier(0.25,0.46,0.45,0.94); overflow: hidden; }
        .portfolio-item:hover { transform: translateY(-20px) scale(1.02); box-shadow: 0 40px 100px rgba(0,0,0,0.6); }
        .portfolio-overlay { position: absolute; top: 50%; left: 50%; transform: translate(-50%,-50%); text-align: center; color: #fff; z-index: 2; }
        .sale-badge { position: absolute; top: 20px; right: 20px; background: linear-gradient(135deg, #ff4444, #ff6666); padding: 1rem 1.5rem; border-radius: 30px; font-weight: 800; box-shadow: 0 10px 30px rgba(255,68,68,0.5); }
        /* Pricing Section */
        .pricing-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 2rem; margin: 4rem 0; width: 100%; }
        .price-card { background: rgba(255,255,255,0.1); backdrop-filter: blur(20px); padding: 2.5rem; border-radius: 25px; text-align: center; border: 1px solid rgba(255,255,255,0.2); transition: all 0.3s; }
        .price-card:hover { transform: translateY(-15px); background: rgba(255,255,255,0.15); }
        .price { font-size: clamp(2.5rem, 8vw, 4rem); font-weight: 900; background: linear-gradient(45deg, #00ff88, #ff00ff); -webkit-background-clip: text; -webkit-text-fill-color: transparent; }
        .old-price { font-size: 1.2rem; text-decoration: line-through; opacity: 0.6; color: #ff4444; }
        /* Responsive */
        @media (max-width: 768px) { .hamburger { display: flex; } .nav-links { position: fixed; left: -100%; top: 70px; flex-direction: column; background: rgba(10,10,10,0.98); width: 100%; padding: 3rem 0; text-align: center; transition: left 0.4s; z-index: 998; backdrop-filter: blur(20px); } .nav-links.active { left: 0; } .portfolio-grid { grid-template-columns: 1fr; } .btn { display: block; margin: 1rem auto; } }
        @media (max-width: 480px) { section { padding: clamp(120px, 25vh, 150px) 0 clamp(90px, 20vh, 120px); } }
    </style>
</head>
<body>
    <!-- Start Animation Preloader -->
    <div class="preloader" id="preloader">
        <div class="logo-spin">ARYAN CODES</div>
        <div class="load-bar"><div class="load-progress"></div></div>
    </div>

    <!-- Sale Banner -->
    <div class="sale-live" id="saleBanner">
        <h3>🔥 FLASH SALE LIVE! Premium Templates 75% OFF</h3>
        <div class="countdown" id="countdown"></div>
    </div>

    <!-- Header -->
    <header>
        <nav class="container">
            <div class="logo">ARYAN CODES</div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#portfolio">Portfolio</a></li>
                <li><a href="#pricing">Pricing</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
            <div class="hamburger" id="hamburger">
                <span></span><span></span><span></span>
            </div>
        </nav>
    </header>

    <!-- Floating Instagram -->
    <a href="https://instagram.com/aaruu_codes" class="insta-fab" target="_blank" title="DM @aaruu_codes for Orders">📸</a>

    <!-- Hero -->
    <section id="home">
        <div class="container">
            <h1>Professional Web Templates</h1>
            <div class="profile-img">AC</div>
            <p>Responsive, Animated, Customizable HTML templates for all occasions. Flash sale - limited time!</p>
            <a href="#portfolio" class="btn">View Portfolio</a>
            <a href="https://wa.me/917772075898?text=Hi! Interested in templates - send prices & demos" class="btn whatsapp-btn">Order WhatsApp</a>
        </div>
    </section>

    <!-- Portfolio -->
    <section id="portfolio">
        <div class="container">
            <h2>Premium Portfolio Showcase</h2>
            <div class="portfolio-grid">
                <div class="portfolio-item" style="background: linear-gradient(45deg, #ff9a9e, #fecfef);" onclick="window.open('aryan-codes-website/templates/anniversary.html','_blank')">
                    <div class="sale-badge">₹199 <span class="old-price">₹999</span></div>
                    <div class="portfolio-overlay">
                        <h3>💕 Anniversary</h3>
                        <p>Romantic animations & timeline</p>
                    </div>
                </div>
                <div class="portfolio-item" style="background: linear-gradient(45deg, #a8edea, #fed6e3);" onclick="window.open('aryan-codes-website/templates/birthday-festival.html','_blank')">
                    <div class="sale-badge">₹299 <span class="old-price">₹1499</span></div>
                    <div class="portfolio-overlay">
                        <h3>🎂 Birthday/Festival</h3>
                        <p>Fireworks, wishes, music</p>
                    </div>
                </div>
                <div class="portfolio-item" style="background: linear-gradient(45deg, #ffecd2, #fcb69f);" onclick="window.open('aryan-codes-website/templates/love-proposal.html','_blank')">
                    <div class="sale-badge">₹399 <span class="old-price">₹1999</span></div>
                    <div class="portfolio-overlay">
                        <h3>💍 Proposal</h3>
                        <p>Interactive heartbeat effects</p>
                    </div>
                </div>
                <div class="portfolio-item" style="background: linear-gradient(45deg, #667eea, #764ba2);" onclick="window.open('aryan-codes-website/templates/hotel.html','_blank')">
                    <div class="sale-badge">₹999 <span class="old-price">₹4999</span></div>
                    <div class="portfolio-overlay">
                        <h3>🏨 Hotel Booking</h3>
                        <p>Professional responsive site</p>
                    </div>
                </div>
                <div class="portfolio-item" style="background: linear-gradient(45deg, #f093fb, #f5576c);" onclick="window.open('aryan-codes-website/templates/ecommerce.html','_blank')">
                    <div class="sale-badge">₹1499 <span class="old-price">₹7999</span></div>
                    <div class="portfolio-overlay">
                        <h3>🛍️ E-Commerce</h3>
                        <p>Shop catalog & cart</p>
                    </div>
                </div>
                <div class="portfolio-item" style="background: linear-gradient(45deg, #4facfe, #00f2fe);" onclick="window.open('aryan-codes-website/templates/portfolio.html','_blank')">
                    <div class="sale-badge">₹2499 <span class="old-price">₹9999</span></div>
                    <div class="portfolio-overlay">
                        <h3>💼 Business Portfolio</h3>
                        <p>Corporate professional site</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Pricing -->
    <section id="pricing">
        <div class="container">
            <h2>Transparent Pricing - DM Instagram for Quote</h2>
            <p>Click prices for instant Instagram DM with your requirements. Custom quotes in 5 mins!</p>
            <div class="pricing-grid">
                <div class="price-card">
                    <div class="price">₹199<span class="old-price">₹999</span></div>
                    <h3>Basic Template</h3>
                    <p>Anniversary/Birthday single page</p>
                    <a href="https://instagram.com/aaruu_codes?text=Hi! Quote for Basic Template ₹199" class="btn insta-btn" target="_blank">Get Quote</a>
                </div>
                <div class="price-card">
                    <div class="price">₹999<span class="old-price">₹4999</span></div>
                    <h3>Professional Site</h3>
                    <p>Hotel/Restaurant multi-page</p>
                    <a href="https://instagram.com/aaruu_codes?text=Hi! Quote for Professional Site ₹999" class="btn insta-btn" target="_blank">Get Quote</a>
                </div>
                <div class="price-card">
                    <div class="price">₹4999<span class="old-price">₹19999</span></div>
                    <h3>Custom E-Commerce</h3>
                    <p>Full shop with payment integration</p>
                    <a href="https://instagram.com/aaruu_codes?text=Hi! Quote for Custom E-Commerce ₹4999" class="btn insta-btn" target="_blank">Get Quote</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact -->
    <section id="contact">
        <div class="container">
            <h2>Ready to Order?</h2>
            <p>Instant delivery | Full support | 100% responsive</p>
            <div style="display: flex; gap: 2rem; flex-wrap: wrap; justify-content: center; margin-top: 3rem;">
                <a href="https://wa.me/917772075898?text=Hi Aryan! Need website quote" class="btn whatsapp-btn">WhatsApp Order</a>
                <a href="https://instagram.com/aaruu_codes" class="btn insta-btn" target="_blank">Instagram DM</a>
            </div>
        </div>
    </section>

    <script>
        // Preloader
        window.addEventListener('load', () => {
            setTimeout(() => document.getElementById('preloader').classList.add('hidden'), 2500);
        });

        // Countdown (10 days)
        let endTime = new Date(Date.now() + 10*24*60*60*1000).getTime();
        setInterval(() => {
            let now = Date.now(), dist = endTime - now;
            if (dist > 0) {
                let d = Math.floor(dist/86400000), h = Math.floor((dist%86400000)/3600000), m = Math.floor((dist%3600000)/60000), s = Math.floor((dist%60000)/1000);
                document.getElementById('countdown').innerHTML = `<span>${d}d</span><span>${h}h</span><span>${m}m</span><span>${s}s</span>`;
            } else {
                document.getElementById('saleBanner').innerHTML = '<h3>Sale Ended!</h3>';
            }
        }, 1000);

        // Mobile menu
        document.getElementById('hamburger').onclick = () => document.querySelector('.nav-links').classList.toggle('active');
        document.querySelectorAll('a[href^="#"]').forEach(a => a.onclick = e => { e.preventDefault(); document.querySelector(a.href).scrollIntoView({behavior:'smooth'}); });

        // Smooth hover effects
        document.querySelectorAll('.portfolio-item, .price-card').forEach(el => {
            el.onmouseenter = () => el.style.transform = 'translateY(-15px) scale(1.02)';
            el.onmouseleave = () => el.style.transform = 'translateY(0) scale(1)';
        });
    </script>
</body>
</html>
