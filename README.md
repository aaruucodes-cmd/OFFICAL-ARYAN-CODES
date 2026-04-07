<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ARYAN CODES | Cyber-Luxury Sale</title>
    <style>
        :root {
            --primary: #00f2fe;
            --secondary: #4facfe;
            --accent: #ff007a;
            --bg-dark: #020205;
            --glass: rgba(255, 255, 255, 0.03);
            --glass-border: rgba(255, 255, 255, 0.1);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; outline: none; }
        
        body {
            font-family: 'Inter', system-ui, -apple-system, sans-serif;
            background-color: var(--bg-dark);
            color: #fff;
            overflow-x: hidden;
            line-height: 1.6;
        }

        /* 3D Particle Canvas Background */
        #bg-canvas {
            position: fixed;
            top: 0;
            left: 0;
            z-index: -1;
            width: 100%;
            height: 100%;
        }

        .container { max-width: 1200px; margin: 0 auto; padding: 0 24px; }

        /* Preloader */
        .preloader {
            position: fixed;
            inset: 0;
            background: var(--bg-dark);
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 10000;
            transition: 0.8s cubic-bezier(0.8, 0, 0.2, 1);
        }
        .preloader.hidden { opacity: 0; visibility: hidden; transform: scale(1.1); }
        .loader-text { 
            font-size: 2rem; font-weight: 900; 
            letter-spacing: 10px; color: var(--primary);
            text-shadow: 0 0 20px var(--primary);
            animation: pulse 1.5s infinite alternate;
        }

        /* Fixed Sale Banner */
        .sale-banner {
            position: fixed;
            top: 0; width: 100%;
            background: linear-gradient(90deg, #ff0055, #ff00aa);
            color: white;
            padding: 12px;
            text-align: center;
            z-index: 2000;
            font-weight: 800;
            text-transform: uppercase;
            box-shadow: 0 5px 20px rgba(255,0,85,0.4);
        }
        .countdown-timer span {
            background: rgba(0,0,0,0.3);
            padding: 4px 10px;
            border-radius: 6px;
            margin: 0 4px;
            font-family: monospace;
            border: 1px solid rgba(255,255,255,0.2);
        }

        /* Header & Nav */
        header {
            position: fixed;
            top: 45px; width: 100%;
            z-index: 1000;
            transition: 0.4s;
        }
        header.scrolled { top: 0; background: rgba(0,0,0,0.8); backdrop-filter: blur(10px); }
        
        nav { display: flex; justify-content: space-between; align-items: center; padding: 20px 0; }
        .logo { font-size: 1.8rem; font-weight: 900; color: #fff; text-decoration: none; letter-spacing: -1px; }
        .logo span { color: var(--primary); }

        .nav-links { display: flex; gap: 30px; list-style: none; }
        .nav-links a { color: #fff; text-decoration: none; font-weight: 500; opacity: 0.7; transition: 0.3s; }
        .nav-links a:hover { opacity: 1; color: var(--primary); }

        /* Hero Section */
        .hero { 
            min-height: 100vh; 
            display: flex; 
            align-items: center; 
            justify-content: center; 
            text-align: center;
            padding-top: 100px;
        }
        .hero-content h1 { 
            font-size: clamp(3rem, 10vw, 6.5rem); 
            line-height: 0.9; margin-bottom: 24px;
            background: linear-gradient(to bottom, #fff 40%, var(--primary));
            -webkit-background-clip: text; -webkit-text-fill-color: transparent;
        }
        .hero-content p { font-size: 1.2rem; opacity: 0.6; max-width: 600px; margin: 0 auto 40px; }

        /* Buttons */
        .btn-group { display: flex; gap: 20px; justify-content: center; flex-wrap: wrap; }
        .btn {
            padding: 16px 40px; border-radius: 100px;
            text-decoration: none; font-weight: 700;
            transition: 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative; overflow: hidden;
            display: flex; align-items: center; gap: 10px;
        }
        .btn-primary { background: var(--primary); color: #000; box-shadow: 0 10px 30px rgba(0,242,254,0.3); }
        .btn-whatsapp { background: #25D366; color: #fff; }
        .btn:hover { transform: translateY(-5px); box-shadow: 0 15px 40px rgba(0,0,0,0.4); }

        /* Portfolio Cards */
        .section-title { font-size: 3rem; text-align: center; margin-bottom: 60px; }
        .portfolio-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); gap: 30px; }
        
        .card {
            background: var(--glass);
            border: 1px solid var(--glass-border);
            border-radius: 30px;
            padding: 10px;
            backdrop-filter: blur(10px);
            transition: 0.5s;
            position: relative;
        }
        .card:hover { border-color: var(--primary); transform: translateY(-10px); background: rgba(255,255,255,0.06); }
        
        .card-img {
            height: 240px; width: 100%; border-radius: 24px;
            background: linear-gradient(45deg, #121212, #252525);
            display: flex; align-items: center; justify-content: center;
            font-size: 3rem; margin-bottom: 20px;
        }
        .card-body { padding: 10px 20px 20px; }
        .card-price { 
            display: flex; align-items: baseline; gap: 10px; margin-bottom: 15px; 
            color: var(--primary); font-size: 1.8rem; font-weight: 800;
        }
        .card-price del { font-size: 1rem; color: rgba(255,255,255,0.3); }

        .tag {
            position: absolute; top: 20px; right: 20px;
            background: var(--accent); padding: 5px 15px;
            border-radius: 100px; font-size: 0.7rem; font-weight: 900;
        }

        /* Contact/Buy Section */
        .contact-box {
            background: linear-gradient(135deg, var(--glass), rgba(0,242,254,0.05));
            border-radius: 40px; padding: 60px;
            text-align: center; margin-top: 100px;
            border: 1px solid var(--glass-border);
        }

        /* Floating IG Icon */
        .ig-float {
            position: fixed; bottom: 30px; right: 30px;
            width: 60px; height: 60px;
            background: linear-gradient(45deg, #f09433, #e6683c, #dc2743, #cc2366, #bc1888);
            border-radius: 20px; display: flex; justify-content: center; align-items: center;
            box-shadow: 0 10px 30px rgba(220, 39, 67, 0.4);
            z-index: 1000; transition: 0.3s;
        }
        .ig-float:hover { transform: scale(1.1) rotate(10deg); }

        /* Animations */
        @keyframes pulse { to { opacity: 0.5; } }
        [data-aos] { opacity: 0; transform: translateY(30px); transition: 0.8s ease-out; }
        [data-aos].visible { opacity: 1; transform: translateY(0); }

        @media (max-width: 768px) {
            .nav-links { display: none; }
            .hero-content h1 { font-size: 3.5rem; }
            .contact-box { padding: 30px; }
        }
    </style>
</head>
<body>

    <canvas id="bg-canvas"></canvas>

    <div class="preloader" id="preloader">
        <div class="loader-text">ARYAN</div>
    </div>

    <div class="sale-banner">
        🔥 Anniversary LIVE SALE is ON! Ends in: 
        <span class="countdown-timer" id="countdown"></span>
    </div>

    <header id="main-header">
        <div class="container">
            <nav>
                <a href="#" class="logo">ARYAN<span>CODES</span></a>
                <ul class="nav-links">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#portfolio">Templates</a></li>
                    <li><a href="#contact">Orders</a></li>
                </ul>
                <a href="https://wa.me/917772075898" class="btn btn-primary" style="padding: 10px 25px;">DM Me</a>
            </nav>
        </div>
    </header>

    <section class="hero" id="home">
        <div class="container hero-content">
            <h1 data-aos>Digital <br>Craftsmanship.</h1>
            <p data-aos>Handcrafted premium responsive templates for life's biggest moments. Anniversary, Proposals, and Professional Portfolios.</p>
            <div class="btn-group" data-aos>
                <a href="#portfolio" class="btn btn-primary">View Designs</a>
                <a href="https://wa.me/917772075898" class="btn btn-whatsapp">Order on WhatsApp</a>
            </div>
        </div>
    </section>

    <section class="container" id="portfolio" style="padding: 100px 0;">
        <h2 class="section-title" data-aos>Luxury Collection</h2>
        <div class="portfolio-grid">
            <div class="card" data-aos>
                <div class="tag">TOP SELLER</div>
                <div class="card-img">💖</div>
                <div class="card-body">
                    <div class="card-price">₹149 <del>₹799</del></div>
                    <h3>Anniversary Premium</h3>
                    <p>Timeline, Music Sync, Photo Gallery.</p>
                </div>
            </div>
            <div class="card" data-aos>
                <div class="card-img">💍</div>
                <div class="card-body">
                    <div class="card-price">₹249 <del>₹1499</del></div>
                    <h3>Proposal Interactive</h3>
                    <p>Interactive "Yes" button & animations.</p>
                </div>
            </div>
            <div class="card" data-aos>
                <div class="card-img">🏨</div>
                <div class="card-body">
                    <div class="card-price">₹999 <del>₹5000</del></div>
                    <h3>Hotel/Shop Business</h3>
                    <p>Professional SEO-friendly architecture.</p>
                </div>
            </div>
        </div>
    </section>

    <section class="container" id="contact" style="padding-bottom: 100px;">
        <div class="contact-box" data-aos>
            <h2>Ready to start your project?</h2>
            <p style="margin-bottom: 30px;">Get your website delivered within 24 hours.</p>
            <a href="https://wa.me/917772075898" class="btn btn-primary" style="margin: 0 auto;">Start Chat Now</a>
        </div>
    </section>

    <a href="https://instagram.com/aaruu_codes" class="ig-float" target="_blank">
        <svg style="width:30px;height:30px" viewBox="0 0 24 24"><path fill="#fff" d="M7.8,2H16.2C19.4,2 22,4.6 22,7.8V16.2A5.8,5.8 0 0,1 16.2,22H7.8C4.6,22 2,19.4 2,16.2V7.8A5.8,5.8 0 0,1 7.8,2M12,7A5,5 0 0,0 7,12A5,5 0 0,0 12,17A5,5 0 0,0 17,12A5,5 0 0,0 12,7M12,9A3,3 0 0,1 15,12A3,3 0 0,1 12,15A3,3 0 0,1 9,12A3,3 0 0,1 12,9M18,7A1,1 0 0,1 17,6A1,1 0 0,1 18,5A1,1 0 0,1 19,6A1,1 0 0,1 18,7Z" /></svg>
    </a>

    <footer style="text-align: center; padding: 40px; opacity: 0.4; font-size: 0.8rem;">
        &copy; 2026 ARYAN CODES | DESIGNED FOR THE FUTURE
    </footer>

    <script>
        // 1. Particle Background Logic
        const canvas = document.getElementById('bg-canvas');
        const ctx = canvas.getContext('2d');
        let particles = [];

        function init() {
            canvas.width = window.innerWidth;
            canvas.height = window.innerHeight;
            particles = [];
            for (let i = 0; i < 80; i++) {
                particles.push({
                    x: Math.random() * canvas.width,
                    y: Math.random() * canvas.height,
                    vx: (Math.random() - 0.5) * 0.5,
                    vy: (Math.random() - 0.5) * 0.5,
                    size: Math.random() * 2
                });
            }
        }

        function draw() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            ctx.fillStyle = '#4facfe';
            ctx.strokeStyle = 'rgba(79, 172, 254, 0.1)';
            particles.forEach((p, i) => {
                p.x += p.vx; p.y += p.vy;
                if (p.x < 0 || p.x > canvas.width) p.vx *= -1;
                if (p.y < 0 || p.y > canvas.height) p.vy *= -1;
                ctx.beginPath(); ctx.arc(p.x, p.y, p.size, 0, Math.PI*2); ctx.fill();
                
                for (let j = i + 1; j < particles.length; j++) {
                    const p2 = particles[j];
                    const dist = Math.hypot(p.x - p2.x, p.y - p2.y);
                    if (dist < 150) {
                        ctx.beginPath(); ctx.moveTo(p.x, p.y); ctx.lineTo(p2.x, p2.y); ctx.stroke();
                    }
                }
            });
            requestAnimationFrame(draw);
        }
        init(); draw();
        window.addEventListener('resize', init);

        // 2. Preloader & AOS
        window.addEventListener('load', () => {
            const preloader = document.getElementById('preloader');
            preloader.classList.add('hidden');
            
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) entry.target.classList.add('visible');
                });
            }, { threshold: 0.1 });
            
            document.querySelectorAll('[data-aos]').forEach(el => observer.observe(el));
        });

        // 3. Countdown Timer
        const saleEnd = Date.now() + (10 * 24 * 60 * 60 * 1000); 
        function updateTimer() {
            const diff = saleEnd - Date.now();
            const d = Math.floor(diff / 86400000);
            const h = Math.floor((diff % 86400000) / 3600000);
            const m = Math.floor((diff % 3600000) / 60000);
            const s = Math.floor((diff % 60000) / 1000);
            document.getElementById('countdown').innerHTML = `<span>${d}d</span>:<span>${h}h</span>:<span>${m}m</span>:<span>${s}s</span>`;
        }
        setInterval(updateTimer, 1000); updateTimer();

        // 4. Header Scroll Effect
        window.addEventListener('scroll', () => {
            const header = document.getElementById('main-header');
            header.classList.toggle('scrolled', window.scrollY > 50);
        });
    </script>
</body>
</html>
