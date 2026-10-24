<!DOCTYPE html>
<html lang="de">
<head>
    <!-- Viewport Meta Tag for Mobile Responsiveness -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta charset="UTF-8">
    <title>Lukokis Boxing - Boxen in Erftstadt</title>
    
    <!-- Google Fonts & Font Awesome Icons -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,400;0,700;0,900;1,400&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <style>
        /* ==========================================================================
           1. RESET & BASE STYLES
           ========================================================================== */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        :root {
            --bg-color: #0a0a0c;
            --card-bg: rgba(18, 18, 22, 0.85);
            --card-border: rgba(255, 255, 255, 0.08);
            --primary-red: #d32f2f;
            --primary-red-hover: #b71c1c;
            --text-light: #f5f5f7;
            --text-muted: #a1a1a6;
            --font-main: 'Montserrat', sans-serif;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-light);
            font-family: var(--font-main);
            line-height: 1.6;
            overflow-x: hidden;
            width: 100%;
        }

        a {
            color: inherit;
            text-decoration: none;
        }

        img {
            max-width: 100%;
            height: auto;
            display: block;
        }

        /* Container Limiters */
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Section Spacing */
        section {
            padding: 80px 0;
            position: relative;
        }

        /* Typography Helpers */
        .section-title {
            font-size: 2.5rem;
            font-weight: 900;
            text-transform: uppercase;
            letter-spacing: 1px;
            text-align: center;
            margin-bottom: 15px;
            color: var(--text-light);
        }

        .section-title span {
            color: var(--primary-red);
        }

        .section-subtitle {
            text-align: center;
            color: var(--text-muted);
            font-size: 1.1rem;
            max-width: 600px;
            margin: 0 auto 50px auto;
        }

        /* Button Styling */
        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            padding: 14px 28px;
            font-weight: 700;
            font-size: 0.95rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            border-radius: 6px;
            transition: all 0.3s ease;
            cursor: pointer;
            border: none;
            gap: 10px;
        }

        .btn-primary {
            background-color: var(--primary-red);
            color: #ffffff;
            box-shadow: 0 4px 15px rgba(211, 47, 47, 0.4);
        }

        .btn-primary:hover {
            background-color: var(--primary-red-hover);
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(211, 47, 47, 0.6);
        }

        .btn-outline {
            background: transparent;
            color: var(--text-light);
            border: 2px solid rgba(255, 255, 255, 0.2);
        }

        .btn-outline:hover {
            border-color: var(--primary-red);
            color: var(--primary-red);
            transform: translateY(-2px);
        }

        /* ==========================================================================
           2. NAVIGATION
           ========================================================================== */
        .navbar {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            background: rgba(10, 10, 12, 0.9);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid var(--card-border);
            padding: 15px 0;
            transition: all 0.3s ease;
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.6rem;
            font-weight: 900;
            letter-spacing: 2px;
            text-transform: uppercase;
            color: #fff;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .logo span {
            color: var(--primary-red);
        }

        .nav-links {
            display: flex;
            gap: 30px;
            list-style: none;
        }

        .nav-links a {
            font-weight: 600;
            font-size: 0.9rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: color 0.3s ease;
        }

        .nav-links a:hover {
            color: var(--primary-red);
        }

        .mobile-toggle {
            display: none;
            background: none;
            border: none;
            color: #fff;
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* ==========================================================================
           3. HERO SECTION (With Halbdurchsichtiger Hintergrund)
           ========================================================================== */
        .hero {
            position: relative;
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding-top: 100px;
            /* Background Stock Photo + Halbdurchsichtiger Overlay */
            background: 
                linear-gradient(180deg, rgba(10, 10, 12, 0.75) 0%, rgba(10, 10, 12, 0.92) 100%),
                url('https://images.unsplash.com/photo-1517649763962-0c623266ddc0?auto=format&fit=crop&w=1920&q=80') center/cover no-repeat fixed;
            text-align: center;
        }

        .hero-content {
            max-width: 850px;
            z-index: 2;
        }

        .hero-badge {
            display: inline-block;
            background: rgba(211, 47, 47, 0.15);
            border: 1px solid var(--primary-red);
            color: var(--primary-red);
            padding: 8px 16px;
            border-radius: 50px;
            font-weight: 700;
            font-size: 0.85rem;
            text-transform: uppercase;
            letter-spacing: 2px;
            margin-bottom: 25px;
        }

        .hero-title {
            font-size: clamp(2.5rem, 6vw, 4.5rem);
            font-weight: 900;
            text-transform: uppercase;
            line-height: 1.1;
            margin-bottom: 25px;
            letter-spacing: 1px;
        }

        .hero-description {
            font-size: 1.2rem;
            color: var(--text-muted);
            margin-bottom: 40px;
            max-width: 650px;
            margin-left: auto;
            margin-right: auto;
        }

        .hero-actions {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: wrap;
        }

        /* ==========================================================================
           4. ABOUT SECTION
           ========================================================================== */
        .about-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
            align-items: center;
        }

        .about-image {
            position: relative;
            border-radius: 12px;
            overflow: hidden;
            border: 1px solid var(--card-border);
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
        }

        .about-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .about-image:hover img {
            transform: scale(1.05);
        }

        .about-text h3 {
            font-size: 1.8rem;
            font-weight: 700;
            margin-bottom: 20px;
            text-transform: uppercase;
        }

        .about-text p {
            color: var(--text-muted);
            margin-bottom: 20px;
        }

        .about-features {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
            margin-top: 30px;
        }

        .feature-item {
            display: flex;
            align-items: center;
            gap: 10px;
            font-weight: 700;
        }

        .feature-item i {
            color: var(--primary-red);
        }

        /* ==========================================================================
           5. SCHEDULE SECTION (Trainingszeiten)
           ========================================================================== */
        .schedule {
            background-color: rgba(18, 18, 22, 0.4);
            border-top: 1px solid var(--card-border);
            border-bottom: 1px solid var(--card-border);
        }

        .schedule-cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
        }

        .schedule-card {
            background: var(--card-bg);
            border: 1px solid var(--card-border);
            border-radius: 12px;
            padding: 35px 25px;
            text-align: center;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .schedule-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: var(--primary-red);
        }

        .schedule-card:hover {
            transform: translateY(-5px);
            border-color: rgba(211, 47, 47, 0.4);
            box-shadow: 0 10px 25px rgba(0,0,0,0.4);
        }

        .schedule-card i.day-icon {
            font-size: 2.2rem;
            color: var(--primary-red);
            margin-bottom: 20px;
        }

        .schedule-card h3 {
            font-size: 1.5rem;
            text-transform: uppercase;
            margin-bottom: 10px;
        }

        .schedule-time {
            font-size: 1.25rem;
            font-weight: 700;
            color: var(--text-light);
            margin-bottom: 15px;
        }

        .schedule-badge {
            display: inline-block;
            background: rgba(255, 255, 255, 0.05);
            padding: 6px 14px;
            border-radius: 20px;
            font-size: 0.85rem;
            color: var(--text-muted);
        }

        /* ==========================================================================
           6. TRAINER TEAM
           ========================================================================== */
        .team-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
            justify-content: center;
        }

        .trainer-card {
            background: var(--card-bg);
            border: 1px solid var(--card-border);
            border-radius: 12px;
            overflow: hidden;
            text-align: center;
            transition: all 0.3s ease;
        }

        .trainer-card:hover {
            transform: translateY(-5px);
            border-color: rgba(211, 47, 47, 0.4);
        }

        .trainer-img {
            width: 100%;
            height: 320px;
            object-fit: cover;
        }

        .trainer-info {
            padding: 25px;
        }

        .trainer-info h3 {
            font-size: 1.4rem;
            text-transform: uppercase;
            margin-bottom: 5px;
        }

        .trainer-role {
            color: var(--primary-red);
            font-weight: 700;
            font-size: 0.85rem;
            text-transform: uppercase;
            margin-bottom: 15px;
            display: block;
        }

        .trainer-social {
            margin-top: 15px;
        }

        .trainer-social a {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            color: var(--text-muted);
            font-size: 0.9rem;
            font-weight: 600;
            transition: color 0.3s ease;
        }

        .trainer-social a:hover {
            color: var(--primary-red);
        }

        /* ==========================================================================
           7. MEMBERSHIP (Mitgliedschaft)
           ========================================================================== */
        .pricing-wrap {
            max-width: 500px;
            margin: 0 auto;
        }

        .pricing-card {
            background: var(--card-bg);
            border: 2px solid var(--primary-red);
            border-radius: 16px;
            padding: 45px 35px;
            text-align: center;
            box-shadow: 0 10px 30px rgba(211, 47, 47, 0.15);
            position: relative;
        }

        .pricing-price {
            font-size: 3.5rem;
            font-weight: 900;
            margin: 20px 0;
            color: #fff;
        }

        .pricing-price span {
            font-size: 1.1rem;
            color: var(--text-muted);
            font-weight: 400;
        }

        .pricing-list {
            list-style: none;
            margin: 30px 0;
            text-align: left;
        }

        .pricing-list li {
            padding: 12px 0;
            border-bottom: 1px solid var(--card-border);
            display: flex;
            align-items: center;
            gap: 12px;
            color: var(--text-muted);
        }

        .pricing-list li i {
            color: var(--primary-red);
        }

        /* ==========================================================================
           8. LOCATION & CONTACT
           ========================================================================== */
        .location-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 40px;
            align-items: center;
        }

        .location-info {
            background: var(--card-bg);
            border: 1px solid var(--card-border);
            padding: 35px;
            border-radius: 12px;
        }

        .info-group {
            display: flex;
            align-items: flex-start;
            gap: 20px;
            margin-bottom: 25px;
        }

        .info-group:last-child {
            margin-bottom: 0;
        }

        .info-group i {
            font-size: 1.5rem;
            color: var(--primary-red);
            margin-top: 5px;
        }

        .info-group h4 {
            font-size: 1.1rem;
            text-transform: uppercase;
            margin-bottom: 5px;
        }

        .info-group p {
            color: var(--text-muted);
        }

        .map-container {
            border-radius: 12px;
            overflow: hidden;
            border: 1px solid var(--card-border);
            height: 380px;
        }

        .map-container iframe {
            width: 100%;
            height: 100%;
            border: 0;
        }

        /* ==========================================================================
           9. FOOTER & MODALS
           ========================================================================== */
        footer {
            background: #050507;
            border-top: 1px solid var(--card-border);
            padding: 40px 0 20px 0;
            text-align: center;
        }

        .footer-social {
            margin-bottom: 20px;
        }

        .footer-social a {
            font-size: 1.5rem;
            margin: 0 12px;
            transition: color 0.3s ease;
        }

        .footer-social a:hover {
            color: var(--primary-red);
        }

        .footer-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-bottom: 20px;
            list-style: none;
            font-size: 0.9rem;
        }

        .footer-links a {
            color: var(--text-muted);
            cursor: pointer;
        }

        .footer-links a:hover {
            color: var(--text-light);
            text-decoration: underline;
        }

        .copyright {
            color: var(--text-muted);
            font-size: 0.85rem;
        }

        /* Modal Styles */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.85);
            backdrop-filter: blur(5px);
            z-index: 2000;
            align-items: center;
            justify-content: center;
            padding: 20px;
        }

        .modal-content {
            background: #121216;
            border: 1px solid var(--card-border);
            border-radius: 12px;
            max-width: 600px;
            width: 100%;
            max-height: 80vh;
            overflow-y: auto;
            padding: 30px;
            position: relative;
            text-align: left;
        }

        .modal-close {
            position: absolute;
            top: 20px;
            right: 20px;
            font-size: 1.5rem;
            color: var(--text-muted);
            cursor: pointer;
            transition: color 0.3s ease;
        }

        .modal-close:hover {
            color: var(--primary-red);
        }

        .modal-content h2 {
            margin-bottom: 20px;
            text-transform: uppercase;
            color: var(--primary-red);
        }

        .modal-content h3 {
            margin: 15px 0 5px 0;
            font-size: 1.1rem;
        }

        .modal-content p {
            color: var(--text-muted);
            font-size: 0.95rem;
            margin-bottom: 10px;
        }

        /* ==========================================================================
           10. MEDIA QUERIES (RESPONSIVE ENGINE)
           ========================================================================== */
        @media (max-width: 768px) {
            .nav-links {
                position: fixed;
                top: 70px;
                left: -100%;
                width: 100%;
                height: calc(100vh - 70px);
                background: #0a0a0c;
                flex-direction: column;
                align-items: center;
                justify-content: center;
                gap: 40px;
                transition: left 0.3s ease;
            }

            .nav-links.active {
                left: 0;
            }

            .mobile-toggle {
                display: block;
            }

            section {
                padding: 60px 0;
            }

            .section-title {
                font-size: 2rem;
            }

            .hero-title {
                font-size: 2.2rem;
            }

            .hero-actions {
                flex-direction: column;
            }

            .hero-actions .btn {
                width: 100%;
            }

            .about-features {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>

    <!-- NAVIGATIONSLEISTE -->
    <nav class="navbar">
        <div class="container nav-container">
            <a href="#" class="logo">
                <i class="fa-solid fa-mitten"></i> LUKOKIS <span>BOXING</span>
            </a>
            <button class="mobile-toggle" id="mobileMenuBtn" aria-label="Menü öffnen">
                <i class="fa-solid fa-bars"></i>
            </button>
            <ul class="nav-links" id="navLinks">
                <li><a href="#about">Über Uns</a></li>
                <li><a href="#schedule">Zeiten</a></li>
                <li><a href="#team">Trainer</a></li>
                <li><a href="#membership">Beitrag</a></li>
                <li><a href="#location">Standort</a></li>
            </ul>
        </div>
    </nav>

    <!-- HERO SEKTION (Halbdurchsichtiger Hintergrund) -->
    <section class="hero">
        <div class="container hero-content">
            <span class="hero-badge"><i class="fa-solid fa-fire"></i> Gratis Probetraining</span>
            <h1 class="hero-title">Trainiere bei wahren Boxprofis</h1>
            <p class="hero-description">
                Egal ob Anfänger, Freizeitsportler oder ambitionierter Athlet – verbessere deine Ausdauer, Technik und mentale Stärke in Erftstadt.
            </p>
            <div class="hero-actions">
                <a href="#schedule" class="btn btn-primary">
                    <i class="fa-solid fa-calendar-check"></i> Gratis Probetraining
                </a>
                <a href="#location" class="btn btn-outline">
                    <i class="fa-solid fa-location-dot"></i> Komm Vorbei
                </a>
            </div>
        </div>
    </section>

    <!-- ÜBER UNS SEKTION -->
    <section id="about">
        <div class="container">
            <div class="about-grid">
                <div class="about-image">
                    <!-- Unsplash Stockphoto Boxgym/Handschuhe -->
                    <img src="https://images.unsplash.com/photo-1549719386-74dfcbf7dbed?auto=format&fit=crop&w=800&q=80" alt="Lukokis Boxing Training">
                </div>
                <div class="about-text">
                    <h2 class="section-title" style="text-align: left;">Der <span>Verein</span></h2>
                    <h3>Disziplin. Respekt. Gemeinschaft.</h3>
                    <p>
                        Bei Lukokis Boxing vereinen wir klassisches Boxhandwerk mit modernem Fitness- und Konditionstraining. Unser Training richtet sich an alle Altersgruppen und Fitnesslevel.
                    </p>
                    <p>
                        Wir legen großen Wert auf eine respektvolle Trainingsatmosphäre, in der jeder über seine Grenzen hinauswachsen kann.
                    </p>
                    <div class="about-features">
                        <div class="feature-item"><i class="fa-solid fa-check"></i> Für jedes Level</div>
                        <div class="feature-item"><i class="fa-solid fa-check"></i> Erfahrene Coaches</div>
                        <div class="feature-item"><i class="fa-solid fa-check"></i> Starker Teamgeist</div>
                        <div class="feature-item"><i class="fa-solid fa-check"></i> Echte Technik</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- TRAININGSZEITEN SEKTION -->
    <section id="schedule" class="schedule">
        <div class="container">
            <h2 class="section-title">Trainings<span>zeiten</span></h2>
            <p class="section-subtitle">Komm einfach während unserer Trainingszeiten für dein kostenloses Probetraining vorbei!</p>
            
            <div class="schedule-cards">
                <div class="schedule-card">
                    <i class="fa-solid fa-calendar-day day-icon"></i>
                    <h3>Montag</h3>
                    <div class="schedule-time">18:00 – 19:30 Uhr</div>
                    <span class="schedule-badge">Alle Leistungsstufen</span>
                </div>
                <div class="schedule-card">
                    <i class="fa-solid fa-calendar-day day-icon"></i>
                    <h3>Samstag</h3>
                    <div class="schedule-time">12:00 – 13:30 Uhr</div>
                    <span class="schedule-badge">Gratis Probetraining</span>
                </div>
            </div>
        </div>
    </section>

    <!-- TRAINER-TEAM SEKTION -->
    <section id="team">
        <div class="container">
            <h2 class="section-title">Trainer <span>Team</span></h2>
            <p class="section-subtitle">Lerne von erfahrenen Trainern mit Leidenschaft für den Sport.</p>
            
            <div class="team-grid">
                <!-- Coach Nathan -->
                <div class="trainer-card">
                    <!-- Unsplash Stockphoto Coach Male 1 -->
                    <img src="https://images.unsplash.com/photo-1583454110551-21f2fa2afe61?auto=format&fit=crop&w=600&q=80" alt="Coach Nathan" class="trainer-img">
                    <div class="trainer-info">
                        <h3>Coach Nathan</h3>
                        <span class="trainer-role">Head Coach</span>
                        <p style="color: var(--text-muted); font-size: 0.9rem;">Spezialist für Technik, Beinarbeit und Wettkampfvorbereitung.</p>
                        <div class="trainer-social">
                            <a href="https://www.instagram.com/p/DUnoQQdDXSa/" target="_blank" rel="noopener">
                                <i class="fa-brands fa-instagram"></i> Instagram Profil
                            </a>
                        </div>
                    </div>
                </div>

                <!-- Coach Metou -->
                <div class="trainer-card">
                    <!-- Unsplash Stockphoto Coach Male 2 -->
                    <img src="https://images.unsplash.com/photo-1517838277536-f5f99be501cd?auto=format&fit=crop&w=600&q=80" alt="Coach Metou" class="trainer-img">
                    <div class="trainer-info">
                        <h3>Coach Metou</h3>
                        <span class="trainer-role">Boxing & Conditioning Coach</span>
                        <p style="color: var(--text-muted); font-size: 0.9rem;">Fokus auf Ausdauer, Kraft und Pratzentraining.</p>
                        <div class="trainer-social">
                            <a href="https://www.instagram.com/p/DWn6g_7DT-O/" target="_blank" rel="noopener">
                                <i class="fa-brands fa-instagram"></i> Instagram Profil
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- MITGLIEDSCHAFT SEKTION -->
    <section id="membership" style="background-color: rgba(18, 18, 22, 0.4); border-top: 1px solid var(--card-border);">
        <div class="container">
            <h2 class="section-title">Mitglied<span>schaft</span></h2>
            <p class="section-subtitle">Faire Preise ohne versteckte Kosten.</p>
            
            <div class="pricing-wrap">
                <div class="pricing-card">
                    <h3>Monatsbeitrag</h3>
                    <div class="pricing-price">35 € <span>/ Monat</span></div>
                    <ul class="pricing-list">
                        <li><i class="fa-solid fa-check"></i> Zugang zu allen Einheiten</li>
                        <li><i class="fa-solid fa-check"></i> Betreuung durch Chef-Coaches</li>
                        <li><i class="fa-solid fa-check"></i> Technik & Konditionstraining</li>
                        <li><i class="fa-solid fa-check"></i> Kostenloses Probetraining inklusive</li>
                    </ul>
                    <a href="#location" class="btn btn-primary" style="width: 100%;">
                        <i class="fa-solid fa-person-running"></i> Probetraining Machen
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- STANDORT SEKTION -->
    <section id="location">
        <div class="container">
            <h2 class="section-title">Unser <span>Standort</span></h2>
            <p class="section-subtitle">Hier findest du uns in Erftstadt.</p>

            <div class="location-grid">
                <div class="location-info">
                    <div class="info-group">
                        <i class="fa-solid fa-location-dot"></i>
                        <div>
                            <h4>Adresse</h4>
                            <p>Herriger Str. 25<br>50374 Erftstadt<br>(In der Tanzschule Latus)</p>
                        </div>
                    </div>
                    <div class="info-group">
                        <i class="fa-solid fa-clock"></i>
                        <div>
                            <h4>Trainingszeiten</h4>
                            <p>Mo: 18:00 – 19:30 Uhr<br>Sa: 12:00 – 13:30 Uhr</p>
                        </div>
                    </div>
                    <div class="info-group">
                        <i class="fa-solid fa-envelope"></i>
                        <div>
                            <h4>Kontakt & Fragen</h4>
                            <p>welias200418@gmail.com</p>
                        </div>
                    </div>
                </div>

                <div class="map-container">
                    <!-- Google Maps Embed for Herriger Str. 25, 50374 Erftstadt -->
                    <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2520.2185202867804!2d6.768393576883262!3d50.80862086214349!2m3!1f0!1f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47bf13264d88e0db%3A0x29649ff5c9f59265!2sHerriger%20Str.%2025%2C%2050374%20Erftstadt!5e0!3m2!1sde!2sde!4v1700000000000!5m2!1sde!2sde" allowfullscreen="" loading="lazy"></iframe>
                </div>
            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer>
        <div class="container">
            <div class="footer-social">
                <a href="https://www.instagram.com/lukokisboxing" target="_blank" aria-label="Instagram" rel="noopener">
                    <i class="fa-brands fa-instagram"></i>
                </a>
            </div>
            <ul class="footer-links">
                <li><a onclick="openModal('impressumModal')">Impressum</a></li>
                <li><a onclick="openModal('datenschutzModal')">Datenschutz</a></li>
            </ul>
            <p class="copyright">&copy; 2026 Lukokis Boxing. Alle Rechte vorbehalten.</p>
        </div>
    </footer>

    <!-- IMPRESSUM MODAL -->
    <div class="modal" id="impressumModal">
        <div class="modal-content">
            <span class="modal-close" onclick="closeModal('impressumModal')">&times;</span>
            <h2>Impressum</h2>
            <p><strong>Angaben gemäß § 5 DDG:</strong></p>
            <p>
                Elias Westphal<br>
                Nordweg 25<br>
                50169 Kerpen<br>
                Deutschland
            </p>
            <h3>Kontakt</h3>
            <p>E-Mail: welias200418@gmail.com</p>
            <h3>Verantwortlich für den Inhalt nach § 18 Abs. 2 MStV</h3>
            <p>
                Elias Westphal<br>
                Nordweg 25, 50169 Kerpen
            </p>
        </div>
    </div>

    <!-- DATENSCHUTZ MODAL -->
    <div class="modal" id="datenschutzModal">
        <div class="modal-content">
            <span class="modal-close" onclick="closeModal('datenschutzModal')">&times;</span>
            <h2>Datenschutzerklärung</h2>
            <h3>1. Datenschutz auf einen Blick</h3>
            <p>Diese Website dient rein zur Information über das Trainingsangebot von Lukokis Boxing. Es werden keine personenbezogenen Daten über Formulare erhoben.</p>
            
            <h3>2. Hosting</h3>
            <p>Diese Website wird extern gehostet (z. B. GitHub Pages / Netlify). Der Hoster erfasst automatisch IP-Adressen und Zugriffsdaten in Server-Logfiles zur Aufrechterhaltung des Betriebs.</p>

            <h3>3. Eingebundene Dienste</h3>
            <p>Zur Darstellung der Anfahrt wird Google Maps verwendet. Beim Aufruf der Karte werden Daten an Google übertragen.</p>
        </div>
    </div>

    <!-- JAVASCRIPT -->
    <script>
        // Mobile Menu Navigation Toggle
        const mobileMenuBtn = document.getElementById('mobileMenuBtn');
        const navLinks = document.getElementById('navLinks');

        mobileMenuBtn.addEventListener('click', () => {
            navLinks.classList.toggle('active');
            const icon = mobileMenuBtn.querySelector('i');
            if(navLinks.classList.contains('active')) {
                icon.classList.remove('fa-bars');
                icon.classList.add('fa-xmark');
            } else {
                icon.classList.remove('fa-xmark');
                icon.classList.add('fa-bars');
            }
        });

        // Close Mobile Menu when clicking link
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                navLinks.classList.remove('active');
                mobileMenuBtn.querySelector('i').classList.remove('fa-xmark');
                mobileMenuBtn.querySelector('i').classList.add('fa-bars');
            });
        });

        // Modal Logic
        function openModal(id) {
            document.getElementById(id).style.display = 'flex';
        }

        function closeModal(id) {
            document.getElementById(id).style.display = 'none';
        }

        window.onclick = function(event) {
            if (event.target.classList.contains('modal')) {
                event.target.style.display = "none";
            }
        }
    </script>
</body>
</html>
