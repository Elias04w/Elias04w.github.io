<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lukokis Boxing – Erftstadt</title>
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700;900&family=Teko:wght@600;700&display=swap" rel="stylesheet">
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        :root {
            --bg-dark: #0a0a0c;
            --bg-card: #141418;
            --primary-red: #d32f2f;
            --primary-red-hover: #f44336;
            --text-main: #ffffff;
            --text-muted: #a0a0aa;
            --border-color: #26262e;
            --font-heading: 'Teko', sans-serif;
            --font-body: 'Montserrat', sans-serif;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--bg-dark);
            color: var(--text-main);
            font-family: var(--font-body);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Container & Utilities */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .section-padding {
            padding: 100px 0;
        }

        .badge-red {
            display: inline-block;
            background-color: var(--primary-red);
            color: #fff;
            padding: 6px 16px;
            font-size: 0.85rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1.5px;
            border-radius: 2px;
            margin-bottom: 20px;
        }

        .section-title {
            font-family: var(--font-heading);
            font-size: 3.5rem;
            text-transform: uppercase;
            letter-spacing: 1.5px;
            line-height: 1;
            margin-bottom: 20px;
        }

        .section-subtitle {
            color: var(--text-muted);
            max-width: 600px;
            margin-bottom: 50px;
            font-size: 1.05rem;
        }

        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            padding: 16px 36px;
            background-color: var(--primary-red);
            color: #fff;
            text-decoration: none;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
            border: 2px solid var(--primary-red);
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .btn:hover {
            background-color: transparent;
            color: var(--primary-red);
            box-shadow: 0 0 20px rgba(211, 47, 47, 0.5);
        }

        .btn-outline {
            background-color: rgba(255, 255, 255, 0.05);
            border-color: rgba(255, 255, 255, 0.3);
            color: #fff;
        }

        .btn-outline:hover {
            background-color: #fff;
            color: #000;
            border-color: #fff;
            box-shadow: 0 0 20px rgba(255, 255, 255, 0.3);
        }

        /* Navigation */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            background-color: rgba(10, 10, 12, 0.9);
            backdrop-filter: blur(12px);
            border-bottom: 1px solid rgba(255, 255, 255, 0.08);
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 80px;
        }

        .logo {
            font-family: var(--font-heading);
            font-size: 2.2rem;
            font-weight: 700;
            color: #fff;
            text-decoration: none;
            letter-spacing: 2px;
            text-transform: uppercase;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .logo span {
            color: var(--primary-red);
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 30px;
        }

        .nav-links a {
            color: var(--text-main);
            text-decoration: none;
            font-weight: 600;
            font-size: 0.9rem;
            text-transform: uppercase;
            letter-spacing: 1.5px;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: var(--primary-red);
        }

        /* OPTIMIERTER MAIN / HERO BEREICH */
        .hero {
            position: relative;
            min-height: 100vh;
            display: flex;
            align-items: center;
            padding-top: 100px;
            padding-bottom: 60px;
            background: 
                linear-gradient(180deg, rgba(10, 10, 12, 0.75) 0%, rgba(10, 10, 12, 0.95) 100%),
                url('https://images.unsplash.com/photo-1549719386-74dfcbf7dbed?q=80&w=1920&auto=format&fit=crop') center/cover no-repeat;
            border-bottom: 1px solid var(--border-color);
        }

        .hero-content {
            max-width: 850px;
        }

        .hero h1 {
            font-family: var(--font-heading);
            font-size: clamp(3.8rem, 8vw, 6.5rem);
            line-height: 0.95;
            text-transform: uppercase;
            letter-spacing: 2px;
            margin-bottom: 25px;
            font-weight: 700;
            text-shadow: 0 10px 30px rgba(0,0,0,0.8);
        }

        .hero h1 span {
            color: var(--primary-red);
            background: linear-gradient(45deg, #d32f2f, #ff6b6b);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero p {
            font-size: 1.25rem;
            color: rgba(255, 255, 255, 0.85);
            margin-bottom: 40px;
            max-width: 650px;
            font-weight: 400;
            text-shadow: 0 2px 10px rgba(0,0,0,0.8);
        }

        .hero-btns {
            display: flex;
            gap: 20px;
            flex-wrap: wrap;
        }

        /* Features Section */
        .about-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .about-card {
            background-color: var(--bg-card);
            padding: 40px;
            border: 1px solid var(--border-color);
            transition: transform 0.3s, border-color 0.3s;
        }

        .about-card:hover {
            transform: translateY(-5px);
            border-color: var(--primary-red);
        }

        .about-icon {
            font-size: 2.5rem;
            color: var(--primary-red);
            margin-bottom: 20px;
        }

        .about-card h3 {
            font-family: var(--font-heading);
            font-size: 2rem;
            text-transform: uppercase;
            margin-bottom: 10px;
        }

        .about-card p {
            color: var(--text-muted);
            font-size: 0.95rem;
        }

        /* Schedule Section */
        .schedule {
            background-color: #0d0d10;
        }

        .schedule-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 30px;
        }

        .schedule-card {
            background-color: var(--bg-card);
            border-left: 4px solid var(--primary-red);
            padding: 35px;
            border-top: 1px solid var(--border-color);
            border-right: 1px solid var(--border-color);
            border-bottom: 1px solid var(--border-color);
        }

        .schedule-day {
            font-family: var(--font-heading);
            font-size: 2.5rem;
            color: #fff;
            text-transform: uppercase;
            line-height: 1;
            margin-bottom: 10px;
        }

        .schedule-time {
            font-size: 1.2rem;
            font-weight: 700;
            color: var(--primary-red);
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .schedule-info {
            color: var(--text-muted);
            font-size: 0.95rem;
        }

        /* Coaches Section */
        .coaches-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
        }

        .coach-card {
            background-color: var(--bg-card);
            border: 1px solid var(--border-color);
            overflow: hidden;
        }

        .coach-img {
            width: 100%;
            height: 380px;
            object-fit: cover;
            filter: grayscale(40%);
            transition: filter 0.3s;
        }

        .coach-card:hover .coach-img {
            filter: grayscale(0%);
        }

        .coach-info {
            padding: 30px;
        }

        .coach-name {
            font-family: var(--font-heading);
            font-size: 2.2rem;
            text-transform: uppercase;
            line-height: 1;
            margin-bottom: 5px;
        }

        .coach-title {
            color: var(--primary-red);
            font-weight: 700;
            font-size: 0.9rem;
            text-transform: uppercase;
            margin-bottom: 15px;
        }

        .coach-link {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            color: #fff;
            text-decoration: none;
            font-size: 0.9rem;
            font-weight: 600;
            margin-top: 15px;
            transition: color 0.3s;
        }

        .coach-link:hover {
            color: var(--primary-red);
        }

        /* Pricing Section */
        .pricing {
            background-color: #0d0d10;
        }

        .pricing-box {
            max-width: 600px;
            margin: 0 auto;
            background-color: var(--bg-card);
            border: 2px solid var(--primary-red);
            padding: 50px;
            text-align: center;
            position: relative;
        }

        .pricing-price {
            font-family: var(--font-heading);
            font-size: 5rem;
            color: #fff;
            line-height: 1;
            margin: 20px 0 10px;
        }

        .pricing-price span {
            font-size: 2rem;
            color: var(--text-muted);
        }

        .pricing-features {
            list-style: none;
            margin: 30px 0;
            text-align: left;
        }

        .pricing-features li {
            padding: 12px 0;
            border-bottom: 1px solid var(--border-color);
            display: flex;
            align-items: center;
            gap: 12px;
            color: var(--text-muted);
        }

        .pricing-features li i {
            color: var(--primary-red);
        }

        /* Location Section */
        .location-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
            align-items: center;
        }

        .address-box {
            background-color: var(--bg-card);
            padding: 25px;
            border: 1px solid var(--border-color);
            margin-bottom: 30px;
        }

        .address-box h4 {
            font-family: var(--font-heading);
            font-size: 1.8rem;
            text-transform: uppercase;
            margin-bottom: 10px;
        }

        .map-container {
            width: 100%;
            height: 380px;
            background-color: var(--bg-card);
            border: 1px solid var(--border-color);
            overflow: hidden;
        }

        .map-container iframe {
            width: 100%;
            height: 100%;
            border: 0;
            filter: grayscale(100%) invert(90%) contrast(120%);
        }

        /* Footer */
        footer {
            background-color: #050507;
            padding: 50px 0 30px;
            border-top: 1px solid var(--border-color);
            text-align: center;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-bottom: 30px;
        }

        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 50px;
            height: 50px;
            background-color: var(--bg-card);
            color: #fff;
            border-radius: 50%;
            text-decoration: none;
            font-size: 1.3rem;
            border: 1px solid var(--border-color);
            transition: all 0.3s;
        }

        .social-links a:hover {
            background-color: var(--primary-red);
            border-color: var(--primary-red);
        }

        .footer-nav {
            display: flex;
            justify-content: center;
            gap: 25px;
            margin-bottom: 30px;
            flex-wrap: wrap;
        }

        .footer-nav a {
            color: var(--text-muted);
            text-decoration: none;
            font-size: 0.9rem;
            cursor: pointer;
        }

        .footer-nav a:hover {
            color: #fff;
        }

        .footer-copy {
            color: #555;
            font-size: 0.85rem;
        }

        /* Modals */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.85);
            z-index: 2000;
            align-items: center;
            justify-content: center;
            padding: 20px;
        }

        .modal-content {
            background-color: var(--bg-card);
            border: 1px solid var(--border-color);
            max-width: 700px;
            width: 100%;
            max-height: 80vh;
            overflow-y: auto;
            padding: 40px;
            position: relative;
        }

        .modal-close {
            position: absolute;
            top: 20px;
            right: 20px;
            font-size: 1.5rem;
            color: var(--text-muted);
            cursor: pointer;
        }

        .modal-close:hover {
            color: #fff;
        }

        .modal h2 {
            font-family: var(--font-heading);
            font-size: 2.5rem;
            margin-bottom: 20px;
            color: var(--primary-red);
        }

        .modal p {
            color: var(--text-muted);
            font-size: 0.95rem;
            margin-bottom: 15px;
        }

        /* Mobile Responsive adjustments */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            .location-grid {
                grid-template-columns: 1fr;
            }
            .section-title {
                font-size: 2.8rem;
            }
            .hero-btns {
                flex-direction: column;
            }
            .btn {
                width: 100%;
            }
        }
    </style>
</head>
<body>

    <!-- Header Navigation -->
    <header>
        <div class="container nav-container">
            <a href="#" class="logo"><i class="fa-solid fa-mitten" style="color: var(--primary-red);"></i> Lukokis <span>Boxing</span></a>
            <ul class="nav-links">
                <li><a href="#about">Über Uns</a></li>
                <li><a href="#schedule">Zeiten</a></li>
                <li><a href="#coaches">Trainer</a></li>
                <li><a href="#pricing">Beitrag</a></li>
                <li><a href="#location">Standort</a></li>
            </ul>
        </div>
    </header>

    <!-- OPTIMIERTER HERO-BEREICH -->
    <section class="hero">
        <div class="container">
            <div class="hero-content">
                <span class="badge-red"><i class="fa-solid fa-fire"></i> Gratis Probetraining in Erftstadt</span>
                <h1>Trainiere bei <span>Wahren Boxprofis</span></h1>
                <p>Egal ob Anfänger, Freizeitsportler oder ambitionierter Athlet – verbessere deine Ausdauer, Technik und mentale Stärke bei Lukokis Boxing.</p>
                <div class="hero-btns">
                    <a href="#schedule" class="btn"><i class="fa-regular fa-calendar-check"></i> Gratis Probetraining</a>
                    <a href="#location" class="btn btn-outline"><i class="fa-solid fa-location-dot"></i> Komm Vorbei</a>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="section-padding">
        <div class="container">
            <span class="badge-red">Unsere Philosophie</span>
            <h2 class="section-title">Keine Ausreden. Nur Boxen.</h2>
            <p class="section-subtitle">Wir bieten ein intensives, diszipliniertes Training für jeden, der über seine Grenzen hinauswachsen möchte.</p>
            
            <div class="about-grid">
                <div class="about-card">
                    <i class="fa-solid fa-mitten about-icon"></i>
                    <h3>Echtes Handwerk</h3>
                    <p>Saubere Beinarbeit, präzise Kombinationen und effektive Deckung – direkt vermittelt von erfahrenen Coaches.</p>
                </div>
                <div class="about-card">
                    <i class="fa-solid fa-heart-pulse about-icon"></i>
                    <h3>Volle Fitness</h3>
                    <p>Steigere deine Ausdauer, Kraft und Schnelligkeit mit motivierenden Drills und intensiven Einheiten.</p>
                </div>
                <div class="about-card">
                    <i class="fa-solid fa-users about-icon"></i>
                    <h3>Für Jeden</h3>
                    <p>Von jung bis alt, vom Anfänger bis zum Wettkämpfer. Bei uns ist jeder willkommen, der hart arbeiten möchte.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Schedule Section -->
    <section id="schedule" class="section-padding schedule">
        <div class="container">
            <span class="badge-red">Trainingszeiten</span>
            <h2 class="section-title">Wann wir trainieren</h2>
            <p class="section-subtitle">Komm einfach spontan zum Gratis Probetraining vorbei!</p>

            <div class="schedule-grid">
                <div class="schedule-card">
                    <div class="schedule-day">Montag</div>
                    <div class="schedule-time"><i class="fa-regular fa-clock"></i> 18:00 – 19:30 Uhr</div>
                    <p class="schedule-info">Boxgrundlagen, Beinarbeit & Partnerübungen für alle Leistungsstufen.</p>
                </div>
                <div class="schedule-card">
                    <div class="schedule-day">Samstag</div>
                    <div class="schedule-time"><i class="fa-regular fa-clock"></i> 12:00 – 13:30 Uhr</div>
                    <p class="schedule-info">Technikfeinschliff, Sparring & Konditionstraining fürs Wochenende.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Coaches Section -->
    <section id="coaches" class="section-padding">
        <div class="container">
            <span class="badge-red">Das Team</span>
            <h2 class="section-title">Unsere Trainer</h2>
            <p class="section-subtitle">Lerne von aktiven Sportlern mit jahrelanger Ringer- und Boxerfahrung.</p>

            <div class="coaches-grid">
                <div class="coach-card">
                    <img src="https://images.unsplash.com/photo-1517838277536-f5f99be501cd?q=80&w=800&auto=format&fit=crop" alt="Coach Nathan" class="coach-img">
                    <div class="coach-info">
                        <div class="coach-name">Coach Nathan</div>
                        <div class="coach-title">Head Coach</div>
                        <p style="color: var(--text-muted); font-size: 0.9rem;">Spezialisiert auf Technik, Ringintelligenz und mentale Stärke.</p>
                        <a href="https://www.instagram.com/p/DUnoQQdDXSa/" target="_blank" class="coach-link">
                            <i class="fa-brands fa-instagram"></i> Instagram Profil
                        </a>
                    </div>
                </div>
                <div class="coach-card">
                    <img src="https://images.unsplash.com/photo-1583454110551-21f2fa2afe61?q=80&w=800&auto=format&fit=crop" alt="Coach Metou" class="coach-img">
                    <div class="coach-info">
                        <div class="coach-name">Coach Metou</div>
                        <div class="coach-title">Boxing & Conditioning</div>
                        <p style="color: var(--text-muted); font-size: 0.9rem;">Experte für Athletik, Schlagkraft und Ausdauer.</p>
                        <a href="https://www.instagram.com/p/DWn6g_7DT-O/" target="_blank" class="coach-link">
                            <i class="fa-brands fa-instagram"></i> Instagram Profil
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Pricing Section -->
    <section id="pricing" class="section-padding pricing">
        <div class="container">
            <div style="text-align: center;">
                <span class="badge-red">Fair & Transparent</span>
                <h2 class="section-title">Mitgliedschaft</h2>
                <p class="section-subtitle" style="margin: 0 auto 40px;">Unkomplizierter Beitrag ohne versteckte Kosten.</p>
            </div>

            <div class="pricing-box">
                <span class="badge-red">All Inclusive</span>
                <div class="pricing-price">35 € <span>/ Monat</span></div>
                <ul class="pricing-features">
                    <li><i class="fa-solid fa-check"></i> Zugang zu allen Trainingseinheiten</li>
                    <li><i class="fa-solid fa-check"></i> Betreuung durch erfahrene Coaches</li>
                    <li><i class="fa-solid fa-check"></i> Individuelle Betreuung im Training</li>
                    <li><i class="fa-solid fa-check"></i> Erste Einheit: Gratis Probetraining</li>
                </ul>
                <a href="#location" class="btn" style="width: 100%; justify-content: center;">Komm einfach vorbei</a>
            </div>
        </div>
    </section>

    <!-- Location Section -->
    <section id="location" class="section-padding">
        <div class="container">
            <div class="location-grid">
                <div class="location-details">
                    <span class="badge-red">Wo du uns findest</span>
                    <h2 class="section-title">Location Erftstadt</h2>
                    <p>Unser Training findet in den Räumlichkeiten der Tanzschule Latus statt. Erstklassige Ausstattung und ideale Bedingungen für dein Box-Workout.</p>
                    
                    <div class="address-box">
                        <h4>Lukokis Boxing</h4>
                        <p style="margin-bottom: 5px;"><i class="fa-solid fa-location-dot" style="color: var(--primary-red);"></i> Herriger Str. 25, 50374 Erftstadt</p>
                        <p style="margin-bottom: 0;"><i class="fa-solid fa-building" style="color: var(--primary-red);"></i> In der Tanzschule Latus</p>
                    </div>

                    <a href="https://www.instagram.com/lukokisboxing" target="_blank" class="btn">
                        <i class="fa-brands fa-instagram"></i> Folge uns auf Instagram
                    </a>
                </div>

                <div class="map-container">
                    <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2520.215886675231!2d6.762883376891054!3d50.80868116139433!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47bf23f0a51c9d4b%3A0x62804b4d63428f58!2sHerriger%20Str.%2025%2C%2050374%20Erftstadt!5e0!3m2!1sde!2sde!4v1700000000000!5m2!1sde!2sde" allowfullscreen="" loading="lazy"></iframe>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="social-links">
                <a href="https://www.instagram.com/lukokisboxing" target="_blank"><i class="fa-brands fa-instagram"></i></a>
            </div>

            <div class="footer-nav">
                <a onclick="openModal('impressum-modal')">Impressum</a>
                <a onclick="openModal('datenschutz-modal')">Datenschutz</a>
            </div>

            <div class="footer-copy">
                &copy; 2026 Lukokis Boxing. Alle Rechte vorbehalten.
            </div>
        </div>
    </footer>

    <!-- Impressum Modal -->
    <div id="impressum-modal" class="modal">
        <div class="modal-content">
            <span class="modal-close" onclick="closeModal('impressum-modal')">&times;</span>
            <h2>Impressum</h2>
            <p><strong>Angaben gemäß § 5 DDG:</strong></p>
            <p>Elias Westphal<br>
            Nordweg 25<br>
            Kerpen</p>
            
            <p><strong>Kontakt:</strong></p>
            <p>E-Mail: welias200418@gmail.com<br>
            Instagram: @lukokisboxing</p>

            <p><strong>Verantwortlich für den Inhalt nach § 18 Abs. 2 MStV:</strong></p>
            <p>Elias Westphal<br>Nordweg 25<br>Kerpen</p>
        </div>
    </div>

    <!-- Datenschutz Modal -->
    <div id="datenschutz-modal" class="modal">
        <div class="modal-content">
            <span class="modal-close" onclick="closeModal('datenschutz-modal')">&times;</span>
            <h2>Datenschutzerklärung</h2>
            <p><strong>1. Datenschutz auf einen Blick</strong></p>
            <p>Wir nehmen den Schutz Ihrer persönlichen Daten sehr ernst. Diese Webseite verarbeitet personenbezogene Daten nur im technisch notwendigen Umfang.</p>
            
            <p><strong>2. Hosting (GitHub Pages)</strong></p>
            <p>Unsere Website wird bei GitHub Pages (GitHub Inc., 88 Colin P Kelly Jr St, San Francisco, CA 94107, USA) gehostet. Bei dem Aufruf der Seiten werden durch den Host automatisiert Log-Dateien erhoben.</p>

            <p><strong>3. Einbindung von Drittanbietern</strong></p>
            <p>Auf dieser Website werden Dienste wie Google Maps zur Kartendarstellung genutzt. Dabei kann Ihre IP-Adresse an den jeweiligen Anbieter übertragen werden.</p>
        </div>
    </div>

    <script>
        function openModal(id) {
            document.getElementById(id).style.display = 'flex';
        }

        function closeModal(id) {
            document.getElementById(id).style.display = 'none';
        }

        window.onclick = function(event) {
            if (event.target.classList.contains('modal')) {
                event.target.style.display = 'none';
            }
        }
    </script>
</body>
</html>
