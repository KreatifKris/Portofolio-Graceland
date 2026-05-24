
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portofolio | Graceland Amadeus Subianto</title>
    
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2 family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">

    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <style>
        /* Variabel CSS untuk Tema Dinamis */
        :root {
            --bg-body: linear-gradient(135deg, #f5f7fa 0%, #e4e8f0 100%);
            --bg-container: #ffffff;
            --bg-card: #f7fafc;
            --text-main: #2d3748;
            --text-muted: #4a5568;
            --text-heading: #1a365d;
            --nav-bg: rgba(255, 255, 255, 0.95);
            --nav-text: #4a5568;
            --shadow: 0 10px 30px rgba(166, 173, 201, 0.2);
            --border-card: #3182ce;
        }

        [data-theme="dark"] {
            --bg-body: linear-gradient(135deg, #0f172a 0%, #1e293b 100%);
            --bg-container: #1e293b;
            --bg-card: #334155;
            --text-main: #e2e8f0;
            --text-muted: #94a3b8;
            --text-heading: #38bdf8;
            --nav-bg: rgba(15, 23, 42, 0.95);
            --nav-text: #cbd5e1;
            --shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
            --border-card: #38bdf8;
        }

        html {
            scroll-behavior: smooth;
        }
        body {
            font-family: 'Inter', sans-serif;
            margin: 0;
            padding: 0;
            background: var(--bg-body);
            color: var(--text-main);
            transition: background 0.3s, color 0.3s;
        }

        /* Header */
        header {
            background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
            color: white;
            padding: 70px 20px;
            text-align: center;
            box-shadow: 0 4px 20px rgba(0,0,0,0.1);
        }
        header h1 {
            margin: 0;
            font-size: 3em;
            font-weight: 700;
            letter-spacing: -1px;
        }
        header p {
            margin: 15px 0 0;
            font-size: 1.2em;
            color: #e2e8f0;
            font-weight: 300;
        }

        /* Navigasi Interaktif */
        nav {
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: var(--nav-bg);
            backdrop-filter: blur(10px);
            padding: 15px;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            transition: padding 0.3s, background-color 0.3s;
        }
        nav.scrolled {
            padding: 10px;
            box-shadow: 0 4px 20px rgba(0,0,0,0.1);
        }
        nav a {
            color: var(--nav-text);
            text-decoration: none;
            margin: 0 15px;
            font-weight: 600;
            font-size: 1em;
            transition: all 0.3s ease;
            padding: 6px 12px;
            border-radius: 5px;
        }
        nav a:hover, nav a.active {
            color: #3182ce; 
            background-color: #ebf8ff;
        }
        [data-theme="dark"] nav a:hover {
            color: #38bdf8;
            background-color: #0f172a;
        }

        /* Tombol Toggle Tema */
        .theme-toggle {
            background: none;
            border: none;
            color: var(--nav-text);
            font-size: 1.2em;
            cursor: pointer;
            padding: 6px 12px;
            margin-left: 15px;
            transition: transform 0.3s, color 0.3s;
        }
        .theme-toggle:hover {
            transform: scale(1.2) rotate(15deg);
            color: #3182ce;
        }

        /* Container Konten Utama */
        .container {
            width: 90%;
            max-width: 950px;
            margin: 40px auto;
            background: var(--bg-container);
            padding: 40px;
            border-radius: 16px;
            box-shadow: var(--shadow);
            transition: background 0.3s, box-shadow 0.3s;
            box-sizing: border-box;
        }

        /* Bagian Section dengan Efek Reveal */
        section {
            margin-bottom: 50px;
            scroll-margin-top: 90px; 
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.6s ease-out, transform 0.6s ease-out;
        }
        section.reveal {
            opacity: 1;
            transform: translateY(0);
        }
        h2 {
            font-size: 1.8em;
            color: var(--text-heading);
            position: relative;
            padding-bottom: 10px;
            margin-bottom: 20px;
        }
        h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 60px;
            height: 4px;
            background: var(--border-card);
            border-radius: 2px;
        }
        p {
            line-height: 1.7;
            color: var(--text-muted);
        }

        ul li {
            margin-bottom: 10px;
            color: var(--text-muted);
        }

        /* Grid & Cards */
        .grid {
            display: flex;
            gap: 25px;
            flex-wrap: wrap; 
            margin-top: 20px;
        }
        .card {
            background: var(--bg-card);
            padding: 25px;
            border-radius: 12px;
            flex: 1; 
            min-width: 260px;
            border-top: 4px solid var(--border-card);
            box-shadow: 0 4px 6px rgba(0,0,0,0.02);
            transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
            box-sizing: border-box;
        }
        .card:hover {
            transform: translateY(-8px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.15);
        }
        .card h3 {
            margin-top: 0;
            color: var(--text-heading);
            font-size: 1.2em;
            margin-bottom: 12px;
        }

        /* Footer */
        footer {
            text-align: center;
            padding: 25px;
            background-color: #1a365d;
            color: #a0aec0;
            margin-top: 60px;
            font-size: 0.9em;
        }

        /* Tombol Media Sosial */
        .sosmed-container {
            margin-top: 20px;
        }
        .btn-sosmed {
            display: inline-block;
            margin: 5px 8px 5px 0;
            padding: 12px 24px;
            background-color: #3182ce;
            color: white;
            text-decoration: none;
            border-radius: 8px;
            font-weight: 600;
            transition: all 0.3s ease;
            box-shadow: 0 4px 6px rgba(49, 130, 206, 0.2);
        }
        .btn-sosmed:hover {
            background-color: #2b6cb0;
            transform: translateY(-3px);
            box-shadow: 0 6px 12px rgba(49, 130, 206, 0.3);
        }
        .btn-github {
            background-color: #2d3748;
        }

        /* Media Queries untuk HP */
        @media (max-width: 768px) {
            header h1 { font-size: 2.2em; }
            nav { flex-wrap: wrap; padding: 10px; }
            nav a { margin: 5px; font-size: 0.9em; }
            .container { width: 95%; padding: 20px; }
            .grid { flex-direction: column; gap: 15px; }
            .btn-sosmed { display: block; text-align: center; margin: 10px 0; }
        }
    </style>
</head>
<body>

    <header>
        <h1>Graceland Amadeus Subianto</h1>
        <p>Siswa SMA | Kreator Digital | Web Developer</p>
    </header>

    <nav id="navbar">
        <a href="#tentang" class="nav-link">Tentang Saya</a>
        <a href="#keterampilan" class="nav-link">Keterampilan</a>
        <a href="#pengalaman" class="nav-link">Pengalaman</a>
        <a href="#kontak" class="nav-link">Kontak</a>
        <button class="theme-toggle" id="themeToggle" aria-label="Ubah Tema">
            <i class="fas fa-moon"></i>
        </button>
    </nav>

    <div class="container">
        
        <section id="tentang">
            <h2>Tentang Saya</h2>
            <p>Perkenalkan nama saya <strong>Graceland Amadeus Subianto</strong> atau biasa dipanggil Graceland. Saya merupakan siswa SMA Petra 4 Sidoarjo yang saat ini menduduki bangku kelas 11. Saya memiliki minat yang besar serta bakat di bidang teknologi, pemrograman web, dan juga strategi media sosial.</p>
        </section>

        <section id="keterampilan">
            <h2>Keterampilan (Skills)</h2>
            <div class="grid">
                <div class="card">
                    <h3>Hard Skills</h3>
                    <ul>
                        <li>Pembuatan konten pemrograman web</li>
                        <li>Menguasai HTML, CSS, dan JavaScript</li>
                        <li>Microsoft Office (Word, Excel, PowerPoint)</li>
                        <li>Video Editing & Videografi</li>
                    </ul>
                </div>
                <div class="card">
                    <h3>Soft Skills</h3>
                    <ul>
                        <li>Public Speaking</li>
                        <li>Komunikasi Interpersonal</li>
                        <li>Manajemen Waktu</li>
                        <li>Berpikir Kreatif & Solutif</li>
                    </ul>
                </div>
            </div>
        </section>

        <section id="pengalaman">
            <h2>Pengalaman & Proyek Sekolah</h2>
            <div class="grid">
                <div class="card">
                    <h3>Juara 2 Konten Kreator</h3>
                    <p>Meraih juara 2 dalam ajang kompetisi pembuatan konten di SMA Petra 4 dengan tema: <em>"74 Tahun Petra Bertumbuh & Berkarya"</em>.</p>
                </div>
                <div class="card">
                    <h3>ELS Jurnalistik</h3>
                    <p>Aktif berkontribusi dan bertanggung jawab penuh dalam proses pengembangan serta pembuatan situs web majalah sekolah (A4).</p>
                </div>
                <div class="card">
                    <h3>Juara 1 Lomba Konten</h3>
                    <p>Meraih juara 1 kompetisi pembuatan konten kreatif bertema <em>"Food Blogger"</em> saat menempuh studi di SMP Petra 4.</p>
                </div>
            </div>
        </section>

        <section id="kontak">
            <h2>Hubungi Saya</h2>
            <p>Saya sangat terbuka untuk berdiskusi, bertukar pikiran, atau berkolaborasi dalam proyek-proyek teknologi dan kreatif lainnya. Silakan hubungi saya melalui:</p>
            <p>
                📧 Email: <strong>amadeusgraceland@gmail.com</strong><br>
                📍 Lokasi: Sidoarjo, Indonesia
            </p>
            
            <div class="sosmed-container">
                <a href="https://www.instagram.com/graceland.amadeus?igsh=MWFweHA0ZXkwdzQzZg==" class="btn-sosmed" target="_blank"><i class="fab fa-instagram"></i> Instagram</a>
                <a href="https://www.tiktok.com/@asel_web_program?_r=1&_t=ZS-96cjTGiLQmr" class="btn-sosmed" target="_blank"><i class="fab fa-tiktok"></i> TikTok</a>
                <a href="https://share.google/TgwFeGnkF6gwm4PP4" class="btn-sosmed btn-github" target="_blank"><i class="fab fa-github"></i> GitHub / KreatifKris</a>
            </div>
        </section>

    </div>

    <footer>
        <p>&copy; 2026 Graceland Amadeus. Dibuat dengan penuh dedikasi sebagai portofolio pribadi.</p>
    </footer>

    <script>
        // 1. Fitur Toggle Dark / Light Mode
        const themeToggle = document.getElementById('themeToggle');
        const themeIcon = themeToggle.querySelector('i');

        themeToggle.addEventListener('click', () => {
            const currentTheme = document.documentElement.getAttribute('data-theme');
            let newTheme = 'light';
            
            if (currentTheme !== 'dark') {
                newTheme = 'dark';
                themeIcon.classList.replace('fa-moon', 'fa-sun');
            } else {
                themeIcon.classList.replace('fa-sun', 'fa-moon');
            }
            
            document.documentElement.setAttribute('data-theme', newTheme);
        });

        // 2. Animasi Perubahan Ukuran Navbar saat Scroll
        const navbar = document.getElementById('navbar');
        window.addEventListener('scroll', () => {
            if (window.scrollY > 50) {
                navbar.classList.add('scrolled');
            } else {
                navbar.classList.remove('scrolled');
            }
        });

        // 3. Scroll Reveal Animation (Elemen Muncul saat Di-scroll)
        const sections = document.querySelectorAll('section');
        const navLinks = document.querySelectorAll('.nav-link');

        const revealOnScroll = () => {
            const triggerBottom = window.innerHeight * 0.85;

            sections.forEach(section => {
                const sectionTop = section.getBoundingClientRect().top;

                if (sectionTop < triggerBottom) {
                    section.classList.add('reveal');
                }
            });

            // Auto-active Menu Navigasi Berdasarkan Posisi Halaman
            let currentSection = "";
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                if (window.pageYOffset >= sectionTop - 100) {
                    currentSection = section.getAttribute('id');
                }
            });

            navLinks.forEach(link => {
                link.classList.remove('active');
                if (link.getAttribute('href').includes(currentSection)) {
                    link.classList.add('active');
                }
            });
        };

        window.addEventListener('scroll', revealOnScroll);
        window.addEventListener('load', revealOnScroll); // Jalankan sekali saat web dimuat
    </script>
</body>



