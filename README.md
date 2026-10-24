<!DOCTYPE html>
<html lang="de" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lukokis Boxing | Erftstadt</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        boxingRed: '#dc2626',
                        boxingDark: '#09090b',
                        boxingCard: '#18181b',
                        boxingBorder: '#27272a'
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    }
                }
            }
        }
    </script>
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800;900&family=Oswald:wght@700&display=swap" rel="stylesheet">
    <!-- FontAwesome for icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        .font-oswald {
            font-family: 'Oswald', sans-serif;
        }
        .hero-gradient {
            background: linear-gradient(180deg, rgba(9,9,11,0.75) 0%, rgba(9,9,11,0.98) 100%), radial-gradient(circle at center, rgba(220,38,38,0.2) 0%, transparent 70%);
        }
    </style>
</head>
<body class="bg-boxingDark text-zinc-100 font-sans antialiased selection:bg-boxingRed selection:text-white">

    <!-- Top Announcement Bar -->
    <div class="bg-boxingRed text-white text-xs sm:text-sm font-bold py-2 px-4 text-center uppercase tracking-wider shadow-md">
        🔥 100% Boxsport • Jeder ist willkommen: Freizeit & Ambition • <span class="underline">Gratis Probetraining jederzeit</span>
    </div>

    <!-- Navigation Bar -->
    <header class="sticky top-0 z-50 bg-boxingDark/95 backdrop-blur border-b border-boxingBorder">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-20 flex items-center justify-between">
            <a href="#" class="flex items-center gap-3">
                <div class="bg-boxingRed text-white font-oswald text-2xl tracking-wider px-3 py-1 rounded shadow-lg">LB</div>
                <div>
                    <span class="font-oswald text-xl sm:text-2xl tracking-wide uppercase block leading-none">Lukokis Boxing</span>
                    <span class="text-xs text-zinc-400 font-semibold tracking-widest uppercase">Erftstadt</span>
                </div>
            </a>

            <!-- Desktop Menu -->
            <nav class="hidden md:flex items-center gap-8 font-semibold text-sm uppercase tracking-wider">
                <a href="#start" class="hover:text-boxingRed transition-colors">Start</a>
                <a href="#about" class="hover:text-boxingRed transition-colors">Über uns</a>
                <a href="#zeiten" class="hover:text-boxingRed transition-colors">Trainingszeiten</a>
                <a href="#trainer" class="hover:text-boxingRed transition-colors">Trainer</a>
                <a href="#preise" class="hover:text-boxingRed transition-colors">Beiträge</a>
                <a href="#kontakt" class="hover:text-boxingRed transition-colors">Kontakt</a>
            </nav>

            <!-- Actions / Insta / CTA -->
            <div class="hidden lg:flex items-center gap-4">
                <a href="https://www.instagram.com/lukokisboxing" target="_blank" rel="noopener noreferrer" class="w-10 h-10 rounded-full bg-zinc-900 border border-boxingBorder flex items-center justify-center text-zinc-300 hover:text-white hover:bg-boxingRed hover:border-boxingRed transition-all">
                    <i class="fa-brands fa-instagram text-lg"></i>
                </a>
                <a href="#kontakt" class="bg-boxingRed text-white font-oswald tracking-wide px-5 py-2.5 rounded uppercase hover:bg-red-700 transition-all shadow-md shadow-red-900/30">
                    Komm vorbei
                </a>
            </div>

            <!-- Mobile Menu Button -->
            <button id="menu-btn" class="md:hidden text-zinc-300 hover:text-white text-2xl p-2 focus:outline-none">
                <i class="fa-solid fa-bars"></i>
            </button>
        </div>

        <!-- Mobile Menu Dropdown -->
        <div id="mobile-menu" class="hidden md:hidden bg-boxingCard border-b border-boxingBorder px-6 py-6 space-y-4">
            <a href="#start" class="block font-semibold text-sm uppercase tracking-wider hover:text-boxingRed">Start</a>
            <a href="#about" class="block font-semibold text-sm uppercase tracking-wider hover:text-boxingRed">Über uns</a>
            <a href="#zeiten" class="block font-semibold text-sm uppercase tracking-wider hover:text-boxingRed">Trainingszeiten</a>
            <a href="#trainer" class="block font-semibold text-sm uppercase tracking-wider hover:text-boxingRed">Trainer</a>
            <a href="#preise" class="block font-semibold text-sm uppercase tracking-wider hover:text-boxingRed">Beiträge</a>
            <a href="#kontakt" class="block font-semibold text-sm uppercase tracking-wider hover:text-boxingRed">Kontakt</a>
            <div class="pt-4 flex items-center justify-between border-t border-boxingBorder">
                <a href="https://www.instagram.com/lukokisboxing" target="_blank" class="text-zinc-300 hover:text-boxingRed flex items-center gap-2 text-sm font-semibold">
                    <i class="fa-brands fa-instagram text-xl"></i> Instagram folgen
                </a>
                <a href="#kontakt" class="bg-boxingRed text-white font-oswald px-4 py-2 rounded uppercase text-sm">Komm vorbei</a>
            </div>
        </div>
    </header>

    <script>
        const menuBtn = document.getElementById('menu-btn');
        const mobileMenu = document.getElementById('mobile-menu');
        menuBtn.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });
        mobileMenu.querySelectorAll('a').forEach(link => {
            link.addEventListener('click', () => mobileMenu.classList.add('hidden'));
        });
    </script>

    <!-- Hero Section -->
    <section id="start" class="relative min-h-[90vh] flex items-center justify-center hero-gradient px-4 py-20 border-b border-boxingBorder">
        <div class="absolute inset-0 -z-10 overflow-hidden opacity-30">
            <!-- Unsplash Hero Boxing Stock Photo -->
            <img src="https://images.unsplash.com/photo-1549719386-74dfcbf7dbed?q=80&w=1920&auto=format&fit=crop" alt="Lukokis Boxing Hero" class="w-full h-full object-cover">
        </div>
        <div class="max-w-5xl mx-auto text-center space-y-6">
            <div class="inline-flex items-center gap-2 bg-red-600/20 border border-boxingRed/50 px-4 py-1.5 rounded-full text-boxingRed font-semibold text-xs sm:text-sm uppercase tracking-widest backdrop-blur-sm">
                <i class="fa-solid fa-fire"></i> <span>Gratis Probetraining für alle</span>
            </div>
            <h1 class="font-oswald text-4xl sm:text-6xl lg:text-7xl uppercase tracking-wider font-extrabold leading-none">
                Disziplin. Kraft. <span class="text-boxingRed">Gemeinschaft.</span>
            </h1>
            <p class="text-zinc-300 text-base sm:text-xl max-w-2xl mx-auto font-medium">
                Egal ob Freizeitsportler oder ambitionierter Athlet – bei Lukokis Boxing in Erftstadt trainierst du mit echten Profis. Ohne Bürokratie, einfach vorbeikommen.
            </p>
            <div class="pt-4 flex flex-col sm:flex-row items-center justify-center gap-4">
                <a href="#kontakt" class="w-full sm:w-auto bg-boxingRed text-white font-oswald tracking-widest text-lg px-8 py-4 rounded uppercase hover:bg-red-700 transition-all shadow-xl shadow-red-900/40 text-center">
                    Komm vorbei (Gratis Probetraining)
                </a>
                <a href="#zeiten" class="w-full sm:w-auto bg-boxingCard border border-boxingBorder text-zinc-200 font-oswald tracking-widest text-lg px-8 py-4 rounded uppercase hover:bg-zinc-800 transition-all text-center">
                    Trainingszeiten ansehen
                </a>
            </div>
            <div class="pt-8 grid grid-cols-1 sm:grid-cols-3 gap-4 max-w-3xl mx-auto text-left">
                <div class="bg-boxingCard/90 border border-boxingBorder p-4 rounded-xl backdrop-blur-md">
                    <span class="text-boxingRed font-oswald text-xl block">01. Standort</span>
                    <span class="text-zinc-400 text-sm">Tanzschule Latus, Erftstadt</span>
                </div>
                <div class="bg-boxingCard/90 border border-boxingBorder p-4 rounded-xl backdrop-blur-md">
                    <span class="text-boxingRed font-oswald text-xl block">02. Preis</span>
                    <span class="text-zinc-400 text-sm">Nur 35 € / Monat (Keine 10er-Karten)</span>
                </div>
                <div class="bg-boxingCard/90 border border-boxingBorder p-4 rounded-xl backdrop-blur-md">
                    <span class="text-boxingRed font-oswald text-xl block">03. Level</span>
                    <span class="text-zinc-400 text-sm">Freizeit & Ambitionierte</span>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-20 px-4 sm:px-6 lg:px-8 bg-boxingDark border-b border-boxingBorder">
        <div class="max-w-7xl mx-auto grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
            <div class="space-y-6">
                <div class="text-boxingRed font-oswald uppercase tracking-widest text-sm">Über den Verein</div>
                <h2 class="font-oswald text-3xl sm:text-5xl uppercase tracking-wide font-bold">
                    Harte Arbeit zahlt sich aus. <span class="text-boxingRed">Keine Ausreden.</span>
                </h2>
                <p class="text-zinc-300 leading-relaxed font-normal">
                    Bei Lukokis Boxing steht der echte Sport im Mittelpunkt. Wir bieten intensives Box- und Fitnesstraining, das dich körperlich und mental stärkt – von Technik über Ausdauer bis Sparring.
                </p>
                <p class="text-zinc-300 leading-relaxed font-normal">
                    Ob du einfach deinen Kopf freibekommen willst, Fett verbrennen oder Wettkampf-Ambitionen hast: Bei uns bist du Teil einer echten Gemeinschaft. Pack deine Sportsachen ein und mach beim <strong class="text-white">Gratis Probetraining</strong> mit!
                </p>
                <div class="flex items-center gap-6 pt-2">
                    <div>
                        <span class="block font-oswald text-3xl text-boxingRed">100%</span>
                        <span class="text-xs text-zinc-400 uppercase tracking-wider font-semibold">Echter Boxsport</span>
                    </div>
                    <div class="w-px h-12 bg-boxingBorder"></div>
                    <div>
                        <span class="block font-oswald text-3xl text-boxingRed">35 €</span>
                        <span class="text-xs text-zinc-400 uppercase tracking-wider font-semibold">Monatsbeitrag</span>
                    </div>
                    <div class="w-px h-12 bg-boxingBorder"></div>
                    <div>
                        <span class="block font-oswald text-3xl text-boxingRed">Gratis</span>
                        <span class="text-xs text-zinc-400 uppercase tracking-wider font-semibold">Erstes Training</span>
                    </div>
                </div>
            </div>
            <div class="relative">
                <div class="aspect-video sm:aspect-square bg-boxingCard border border-boxingBorder rounded-2xl overflow-hidden relative shadow-2xl">
                    <!-- Unsplash Gym/Training Stock Photo -->
                    <img src="https://images.unsplash.com/photo-1517838277536-f5f99be501cd?q=80&w=1000&auto=format&fit=crop" alt="Boxen Gym Equipment" class="w-full h-full object-cover">
                    <div class="absolute inset-0 bg-gradient-to-t from-boxingDark via-transparent to-transparent opacity-80"></div>
                    <div class="absolute bottom-6 left-6 right-6">
                        <span class="bg-boxingRed text-white text-xs font-bold uppercase px-3 py-1 rounded">Erftstadt</span>
                        <h3 class="font-oswald text-2xl uppercase mt-2">Tanzschule Latus</h3>
                        <p class="text-sm text-zinc-300">Herriger Str. 25, 50321 Erftstadt</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Trainingszeiten & Ort -->
    <section id="zeiten" class="py-20 px-4 sm:px-6 lg:px-8 bg-zinc-950 border-b border-boxingBorder">
        <div class="max-w-7xl mx-auto space-y-12">
            <div class="text-center space-y-3">
                <span class="text-boxingRed font-oswald uppercase tracking-widest text-sm">Wann & Wo</span>
                <h2 class="font-oswald text-3xl sm:text-5xl uppercase tracking-wide font-bold">Trainingszeiten & Standort</h2>
                <p class="text-zinc-400 max-w-xl mx-auto">Keine Voranmeldung nötig – komm einfach pünktlich in Trainingskleidung vorbei!</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-8 max-w-4xl mx-auto">
                <!-- Standort Info Card -->
                <div class="bg-boxingCard border border-boxingBorder p-8 rounded-2xl flex flex-col justify-between space-y-6 shadow-xl relative overflow-hidden">
                    <div class="space-y-4">
                        <div class="w-12 h-12 rounded-xl bg-boxingRed/10 border border-boxingRed/30 flex items-center justify-center text-boxingRed text-xl">
                            <i class="fa-solid fa-location-dot"></i>
                        </div>
                        <h3 class="font-oswald text-2xl uppercase tracking-wide">Trainingsort</h3>
                        <p class="text-zinc-300 font-medium">
                            <strong class="text-white block text-lg mb-1">Tanzschule Latus</strong>
                            Herriger Str. 25<br>
                            50321 Erftstadt
                        </p>
                    </div>
                    <div class="pt-4 border-t border-boxingBorder">
                        <span class="text-xs text-boxingRed uppercase font-bold tracking-wider block mb-1">Was mitbringen?</span>
                        <p class="text-xs text-zinc-400">Sportbekleidung, saubere Turnschuhe, Handtuch & Trinkflasche.</p>
                    </div>
                </div>

                <!-- Schedule Card -->
                <div class="bg-boxingCard border border-boxingBorder p-8 rounded-2xl flex flex-col justify-between space-y-6 shadow-xl relative overflow-hidden">
                    <div class="space-y-4">
                        <div class="w-12 h-12 rounded-xl bg-boxingRed/10 border border-boxingRed/30 flex items-center justify-center text-boxingRed text-xl">
                            <i class="fa-regular fa-clock"></i>
                        </div>
                        <h3 class="font-oswald text-2xl uppercase tracking-wide">Reguläre Zeiten</h3>
                        <div class="space-y-3">
                            <div class="flex justify-between items-center pb-3 border-b border-boxingBorder">
                                <span class="font-semibold text-zinc-200">Montag</span>
                                <span class="bg-zinc-900 px-3 py-1 rounded text-boxingRed font-oswald tracking-wider">18:00 Uhr</span>
                            </div>
                            <div class="flex justify-between items-center pb-3 border-b border-boxingBorder">
                                <span class="font-semibold text-zinc-200">Samstag</span>
                                <span class="bg-zinc-900 px-3 py-1 rounded text-boxingRed font-oswald tracking-wider">12:00 Uhr</span>
                            </div>
                        </div>
                    </div>
                    <div class="pt-4 border-t border-boxingBorder">
                        <div class="flex items-center gap-2 text-boxingRed font-semibold text-sm">
                            <i class="fa-solid fa-circle-check"></i>
                            <span>Gratis Probetraining bei jedem Termin</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Trainer Section -->
    <section id="trainer" class="py-20 px-4 sm:px-6 lg:px-8 bg-boxingDark border-b border-boxingBorder">
        <div class="max-w-7xl mx-auto space-y-12">
            <div class="text-center space-y-3">
                <span class="text-boxingRed font-oswald uppercase tracking-widest text-sm">Coaching</span>
                <h2 class="font-oswald text-3xl sm:text-5xl uppercase tracking-wide font-bold">Das Trainer-Team</h2>
                <p class="text-zinc-400 max-w-xl mx-auto">Erfahrene Coaches mit Leidenschaft für echten Boxsport.</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-8 max-w-4xl mx-auto">
                <!-- Coach Nathan -->
                <div class="bg-boxingCard border border-boxingBorder rounded-2xl overflow-hidden group shadow-xl">
                    <div class="h-80 overflow-hidden relative bg-zinc-900">
                        <!-- Unsplash Athletic Coach Stock Photo -->
                        <img src="https://images.unsplash.com/photo-1583454110551-21f2fa2afe61?q=80&w=800&auto=format&fit=crop" alt="Coach Nathan" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500">
                        <div class="absolute inset-0 bg-gradient-to-t from-boxingCard via-transparent to-transparent"></div>
                        <span class="absolute top-4 right-4 bg-boxingRed text-white text-xs font-bold uppercase px-3 py-1 rounded">Head Coach</span>
                    </div>
                    <div class="p-6 space-y-4">
                        <h3 class="font-oswald text-3xl uppercase tracking-wide">Coach Nathan</h3>
                        <p class="text-zinc-400 text-sm leading-relaxed">
                            Technik, Kondition und mentale Stärke. Nathan fordert jeden Athleten individuell – egal ob Anfänger beim Probetraining oder erfahrener Boxsportler.
                        </p>
                        <div class="pt-2 flex items-center justify-between border-t border-boxingBorder">
                            <span class="text-xs text-zinc-500 uppercase tracking-widest font-semibold">Instagram Profile</span>
                            <a href="https://www.instagram.com/p/DUnoQQdDXSa/" target="_blank" rel="noopener noreferrer" class="inline-flex items-center gap-2 bg-zinc-900 hover:bg-boxingRed text-zinc-200 hover:text-white px-4 py-2 rounded text-xs uppercase font-bold transition-all border border-boxingBorder">
                                <i class="fa-brands fa-instagram text-base"></i> Beitrag ansehen
                            </a>
                        </div>
                    </div>
                </div>

                <!-- Coach Metou -->
                <div class="bg-boxingCard border border-boxingBorder rounded-2xl overflow-hidden group shadow-xl">
                    <div class="h-80 overflow-hidden relative bg-zinc-900">
                        <!-- Unsplash Athletic Coach Stock Photo 2 -->
                        <img src="https://images.unsplash.com/photo-1517838277536-f5f99be501cd?q=80&w=800&auto=format&fit=crop" alt="Coach Metou" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500">
                        <div class="absolute inset-0 bg-gradient-to-t from-boxingCard via-transparent to-transparent"></div>
                        <span class="absolute top-4 right-4 bg-boxingRed text-white text-xs font-bold uppercase px-3 py-1 rounded">Boxing Coach</span>
                    </div>
                    <div class="p-6 space-y-4">
                        <h3 class="font-oswald text-3xl uppercase tracking-wide">Coach Metou</h3>
                        <p class="text-zinc-400 text-sm leading-relaxed">
                            Fokus auf saubere Beinarbeit, harte Kombinationen und echten Ring-Instinkt. Metou bringt dich bei jeder Trainingseinheit an dein nächstes Level.
                        </p>
                        <div class="pt-2 flex items-center justify-between border-t border-boxingBorder">
                            <span class="text-xs text-zinc-500 uppercase tracking-widest font-semibold">Instagram Profile</span>
                            <a href="https://www.instagram.com/p/DWn6g_7DT-O/" target="_blank" rel="noopener noreferrer" class="inline-flex items-center gap-2 bg-zinc-900 hover:bg-boxingRed text-zinc-200 hover:text-white px-4 py-2 rounded text-xs uppercase font-bold transition-all border border-boxingBorder">
                                <i class="fa-brands fa-instagram text-base"></i> Beitrag ansehen
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Mitgliedsbeiträge -->
    <section id="preise" class="py-20 px-4 sm:px-6 lg:px-8 bg-zinc-950 border-b border-boxingBorder">
        <div class="max-w-4xl mx-auto space-y-12">
            <div class="text-center space-y-3">
                <span class="text-boxingRed font-oswald uppercase tracking-widest text-sm">Transparenz</span>
                <h2 class="font-oswald text-3xl sm:text-5xl uppercase tracking-wide font-bold">Mitgliedsbeitrag</h2>
                <p class="text-zinc-400 max-w-lg mx-auto">Einfache und faire Preise ohne versteckte Kosten.</p>
            </div>

            <!-- Price Card -->
            <div class="bg-boxingCard border-2 border-boxingRed/80 rounded-3xl p-8 sm:p-12 shadow-2xl relative overflow-hidden">
                <div class="absolute -right-16 -top-16 w-48 h-48 bg-boxingRed/10 rounded-full blur-3xl pointer-events-none"></div>
                <div class="flex flex-col md:flex-row items-center justify-between gap-8">
                    <div class="space-y-4 text-center md:text-left">
                        <span class="bg-boxingRed text-white text-xs font-bold uppercase tracking-widest px-3 py-1 rounded">Standard Mitgliedschaft</span>
                        <h3 class="font-oswald text-4xl uppercase">Monatsbeitrag</h3>
                        <p class="text-zinc-400 text-sm max-w-md">
                            Keine versteckten Verträge, keine 10er-Karten oder Einzeltickets. Du zahlst einen transparenten Monatsbeitrag und kannst an allen Einheiten teilnehmen.
                        </p>
                        <ul class="space-y-2 text-sm text-zinc-300 pt-2 inline-block text-left">
                            <li class="flex items-center gap-2"><i class="fa-solid fa-check text-boxingRed"></i> Erstes Training <strong>100% Gratis Probetraining</strong></li>
                            <li class="flex items-center gap-2"><i class="fa-solid fa-check text-boxingRed"></i> Montag & Samstag Training</li>
                            <li class="flex items-center gap-2"><i class="fa-solid fa-check text-boxingRed"></i> Coaching durch Nathan & Metou</li>
                        </ul>
                    </div>
                    <div class="text-center bg-zinc-900/80 border border-boxingBorder p-8 rounded-2xl min-w-[240px]">
                        <span class="text-xs uppercase text-zinc-400 tracking-wider font-semibold block mb-1">Beitrag</span>
                        <div class="font-oswald text-6xl text-white font-bold">35 <span class="text-boxingRed text-3xl">€</span></div>
                        <span class="text-xs text-zinc-500 block mt-2">Pro Monat / Flexibel</span>
                        <div class="mt-6">
                            <a href="#kontakt" class="block w-full bg-boxingRed text-white font-oswald uppercase py-3 rounded hover:bg-red-700 transition-all text-center">
                                Probetraining machen
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Gallery Stock Showcase -->
    <section class="py-16 bg-boxingDark border-b border-boxingBorder">
        <div class="max-w-7xl mx-auto px-4 grid grid-cols-2 md:grid-cols-4 gap-4">
            <div class="h-48 rounded-xl overflow-hidden border border-boxingBorder">
                <img src="https://images.unsplash.com/photo-1517838277536-f5f99be501cd?q=80&w=600&auto=format&fit=crop" alt="Gallery 1" class="w-full h-full object-cover hover:scale-110 transition-transform duration-300">
            </div>
            <div class="h-48 rounded-xl overflow-hidden border border-boxingBorder">
                <img src="https://images.unsplash.com/photo-1549719386-74dfcbf7dbed?q=80&w=600&auto=format&fit=crop" alt="Gallery 2" class="w-full h-full object-cover hover:scale-110 transition-transform duration-300">
            </div>
            <div class="h-48 rounded-xl overflow-hidden border border-boxingBorder">
                <img src="https://images.unsplash.com/photo-1599058945522-28d584b6f0ff?q=80&w=600&auto=format&fit=crop" alt="Gallery 3" class="w-full h-full object-cover hover:scale-110 transition-transform duration-300">
            </div>
            <div class="h-48 rounded-xl overflow-hidden border border-boxingBorder">
                <img src="https://images.unsplash.com/photo-1583454110551-21f2fa2afe61?q=80&w=600&auto=format&fit=crop" alt="Gallery 4" class="w-full h-full object-cover hover:scale-110 transition-transform duration-300">
            </div>
        </div>
    </section>

    <!-- Kontakt & Anfahrt -->
    <section id="kontakt" class="py-20 px-4 sm:px-6 lg:px-8 bg-boxingDark">
        <div class="max-w-5xl mx-auto space-y-12">
            <div class="text-center space-y-3">
                <span class="text-boxingRed font-oswald uppercase tracking-widest text-sm">Einfach vorbeikommen</span>
                <h2 class="font-oswald text-3xl sm:text-5xl uppercase tracking-wide font-bold">Komm zum Training</h2>
                <p class="text-zinc-400 max-w-xl mx-auto">Du brauchst dich nicht vorher anzumelden. Pack einfach deine Sachen ein und schau vorbei.</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                <div class="bg-boxingCard border border-boxingBorder p-6 rounded-2xl text-center space-y-3">
                    <div class="w-12 h-12 bg-boxingRed/10 border border-boxingRed/30 text-boxingRed rounded-full flex items-center justify-center mx-auto text-xl">
                        <i class="fa-solid fa-location-dot"></i>
                    </div>
                    <h3 class="font-oswald text-xl uppercase">Adresse</h3>
                    <p class="text-zinc-400 text-sm">Tanzschule Latus<br>Herriger Str. 25<br>50321 Erftstadt</p>
                </div>

                <div class="bg-boxingCard border border-boxingBorder p-6 rounded-2xl text-center space-y-3">
                    <div class="w-12 h-12 bg-boxingRed/10 border border-boxingRed/30 text-boxingRed rounded-full flex items-center justify-center mx-auto text-xl">
                        <i class="fa-solid fa-envelope"></i>
                    </div>
                    <h3 class="font-oswald text-xl uppercase">E-Mail</h3>
                    <p class="text-zinc-400 text-sm">Fragen?<br><a href="mailto:info@lukokis-boxing.de" class="text-boxingRed hover:underline font-semibold">info@lukokis-boxing.de</a></p>
                </div>

                <div class="bg-boxingCard border border-boxingBorder p-6 rounded-2xl text-center space-y-3">
                    <div class="w-12 h-12 bg-boxingRed/10 border border-boxingRed/30 text-boxingRed rounded-full flex items-center justify-center mx-auto text-xl">
                        <i class="fa-brands fa-instagram"></i>
                    </div>
                    <h3 class="font-oswald text-xl uppercase">Social Media</h3>
                    <p class="text-zinc-400 text-sm">Folge uns auf Instagram<br><a href="https://www.instagram.com/lukokisboxing" target="_blank" class="text-boxingRed hover:underline font-semibold">@lukokisboxing</a></p>
                </div>
            </div>

            <!-- Call to action card -->
            <div class="bg-gradient-to-r from-red-950/60 to-boxingCard border border-boxingRed/40 p-8 rounded-2xl text-center space-y-4">
                <h3 class="font-oswald text-2xl sm:text-3xl uppercase">Dein erstes Training ist komplett kostenlos!</h3>
                <p class="text-zinc-300 text-sm max-w-xl mx-auto">
                    Komm am nächsten Montag um 18:00 Uhr oder Samstag um 12:00 Uhr vorbei. Nathan und Metou freuen sich auf dich!
                </p>
                <div class="pt-2">
                    <a href="https://www.instagram.com/lukokisboxing" target="_blank" class="inline-flex items-center gap-2 bg-boxingRed text-white font-oswald px-6 py-3 rounded uppercase hover:bg-red-700 transition-all">
                        <i class="fa-brands fa-instagram"></i> Fragen stellen auf Instagram
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-zinc-950 border-t border-boxingBorder py-12 px-4 sm:px-6 lg:px-8 text-zinc-400 text-sm">
        <div class="max-w-7xl mx-auto flex flex-col md:flex-row items-center justify-between gap-6">
            <div class="flex items-center gap-3">
                <div class="bg-boxingRed text-white font-oswald text-xl px-2.5 py-0.5 rounded">LB</div>
                <span class="font-oswald text-lg uppercase tracking-wider text-white">Lukokis Boxing Erftstadt</span>
            </div>
            <div class="flex flex-wrap items-center justify-center gap-6 font-semibold">
                <a href="#start" class="hover:text-boxingRed transition-colors">Start</a>
                <a href="#about" class="hover:text-boxingRed transition-colors">Über uns</a>
                <a href="#zeiten" class="hover:text-boxingRed transition-colors">Zeiten</a>
                <a href="#trainer" class="hover:text-boxingRed transition-colors">Trainer</a>
                <a href="#preise" class="hover:text-boxingRed transition-colors">Beiträge</a>
                <button onclick="openModal('impressum-modal')" class="hover:text-boxingRed transition-colors uppercase">Impressum</button>
                <button onclick="openModal('datenschutz-modal')" class="hover:text-boxingRed transition-colors uppercase">Datenschutz</button>
            </div>
            <div class="text-xs text-zinc-500 text-center md:text-right">
                © 2026 Lukokis Boxing. Alle Rechte vorbehalten.
            </div>
        </div>
    </footer>

    <!-- Impressum Modal (Elias' Data) -->
    <div id="impressum-modal" class="fixed inset-0 z-50 hidden bg-black/80 backdrop-blur-sm flex items-center justify-center p-4 overflow-y-auto">
        <div class="bg-boxingCard border border-boxingBorder max-w-2xl w-full rounded-2xl p-6 sm:p-8 relative space-y-6 max-h-[90vh] overflow-y-auto">
            <button onclick="closeModal('impressum-modal')" class="absolute top-4 right-4 text-zinc-400 hover:text-white text-xl">
                <i class="fa-solid fa-xmark"></i>
            </button>
            <h2 class="font-oswald text-3xl uppercase text-white">Impressum</h2>
            <div class="space-y-4 text-zinc-300 text-sm leading-relaxed">
                <div>
                    <h3 class="font-bold text-white uppercase text-xs text-boxingRed tracking-wider">Angaben gemäß § 5 DDG (Betreiber)</h3>
                    <p class="font-semibold text-white">Elias</p>
                    <p><br>Nordweg 25<br>50169 Kerpen<br>Deutschland</p>
                </div>
                <div>
                    <h3 class="font-bold text-white uppercase text-xs text-boxingRed tracking-wider">Kontakt</h3>
                    <p>E-Mail: welias200418@gmail.com</p>
                </div>
                <div>
                    <h3 class="font-bold text-white uppercase text-xs text-boxingRed tracking-wider">Verantwortlich für den Inhalt nach § 18 Abs. 2 MStV</h3>
                    <p>Elias<br>Nordweg 25<br>50169 Kerpen<br>Deutschland</p>
                </div>
                <div class="text-xs text-zinc-500 pt-2 border-t border-boxingBorder">
                    Hinweis: Das Impressum wird bei Bedarf um weitere behördliche Angaben oder Steuernummern ergänzt.
                </div>
            </div>
            <div class="pt-4 border-t border-boxingBorder text-right">
                <button onclick="closeModal('impressum-modal')" class="bg-zinc-800 hover:bg-zinc-700 text-white font-oswald uppercase px-5 py-2 rounded text-sm">Schließen</button>
            </div>
        </div>
    </div>

    <!-- Datenschutz Modal -->
    <div id="datenschutz-modal" class="fixed inset-0 z-50 hidden bg-black/80 backdrop-blur-sm flex items-center justify-center p-4 overflow-y-auto">
        <div class="bg-boxingCard border border-boxingBorder max-w-2xl w-full rounded-2xl p-6 sm:p-8 relative space-y-6 max-h-[90vh] overflow-y-auto">
            <button onclick="closeModal('datenschutz-modal')" class="absolute top-4 right-4 text-zinc-400 hover:text-white text-xl">
                <i class="fa-solid fa-xmark"></i>
            </button>
            <h2 class="font-oswald text-3xl uppercase text-white">Datenschutzerklärung</h2>
            <div class="space-y-4 text-zinc-300 text-sm leading-relaxed">
                <div>
                    <h3 class="font-bold text-white uppercase text-xs text-boxingRed tracking-wider">1. Datenschutz auf einen Blick</h3>
                    <p>Die folgenden Hinweise geben einen einfachen Überblick darüber, was mit Ihren personenbezogenen Daten passiert, wenn Sie unsere Website besuchen.</p>
                </div>
                <div>
                    <h3 class="font-bold text-white uppercase text-xs text-boxingRed tracking-wider">2. Hosting</h3>
                    <p>Diese Website wird bei einem externen Dienstleister gehostet. Personenbezogene Daten, die auf dieser Website erfasst werden, werden auf den Servern des Hosters gespeichert (z.B. IP-Adressen in Server-Logfiles).</p>
                </div>
                <div>
                    <h3 class="font-bold text-white uppercase text-xs text-boxingRed tracking-wider">3. Instagram Verlinkungen</h3>
                    <p>Auf unserer Website verlinken wir auf unser Profil bei Instagram (Meta Platforms Ireland Limited). Beim Anklicken der Verlinkung verlassen Sie unsere Seite.</p>
                </div>
            </div>
            <div class="pt-4 border-t border-boxingBorder text-right">
                <button onclick="closeModal('datenschutz-modal')" class="bg-zinc-800 hover:bg-zinc-700 text-white font-oswald uppercase px-5 py-2 rounded text-sm">Schließen</button>
            </div>
        </div>
    </div>

    <script>
        function openModal(modalId) {
            document.getElementById(modalId).classList.remove('hidden');
        }
        function closeModal(modalId) {
            document.getElementById(modalId).classList.add('hidden');
        }
        window.onclick = function(event) {
            if (event.target.id === 'impressum-modal') closeModal('impressum-modal');
            if (event.target.id === 'datenschutz-modal') closeModal('datenschutz-modal');
        }
    </script>

</body>
</html>
