
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portofolio | Graceland Amadeus Subianto</title>
    
    <!-- Google Fonts untuk tampilan font yang lebih modern -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">

    <!-- CSS untuk desain modern dan interaktif -->
    <style>
        /* Pengaturan Dasar */
        html {
            scroll-behavior: smooth; /* Efek scroll halus */
        }
        body {
            font-family: 'Inter', sans-serif;
            margin: 0;
            padding: 0;
            background: linear-gradient(135deg, #f5f7fa 0%, #e4e8f0 100%); /* Background gradient lembut */
            color: #2d3748;
        }

        /* Bagian Header (Atas) */
        header {
            background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%); /* Gradient tech-blue */
            color: white;
            padding: 60px 20px;
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

        /* Bagian Navigasi (Menu) */
        nav {
            display: flex;
            justify-content: center;
            background-color: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px); /* Efek blur blur modern */
            padding: 15px;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
        }
        nav a {
            color: #4a5568;
            text-decoration: none;
            margin: 0 20px;
            font-weight: 600;
            font-size: 1em;
            transition: all 0.3s ease;
            padding: 5px 10px;
            border-radius: 5px;
        }
        nav a:hover {
            color: #3182ce; 
            background-color: #ebf8ff;
        }

        /* Kotak Konten Utama */
        .container {
            width: 90%;
            max-width: 950px;
            margin: 40px auto;
            background: white;
            padding: 40px;
            border-radius: 16px;
            box-shadow: 0 10px 30px rgba(166, 173, 201, 0.2);
        }

        /* Pengaturan Setiap Bagian (Section) */
        section {
            margin-bottom: 50px;
            scroll-margin-top: 90px; 
        }
        h2 {
            font-size: 1.8em;
            color: #1a365d;
            position: relative;
            padding-bottom: 10px;
            margin-bottom: 20px;
        }
        /* Garis bawah h2 yang lebih modern */
        h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 60px;
            height: 4px;
            background: #3182ce;
            border-radius: 2px;
        }
        p {
            line-height: 1.7;
            color: #4a5568;
        }

        /* List Kustom */
        ul {
            padding-left: 20px;
        }
        ul li {
            margin-bottom: 10px;
            color: #4a5568;
        }

        /* Pengaturan Kotak-kotak Kecil (Card) */
        .grid {
            display: flex;
            gap: 25px;
            flex-wrap: wrap; 
            margin-top: 20px;
        }
        .card {
            background: #f7fafc;
            padding: 25px;
            border-radius: 12px;
            flex: 1; 
            min-width: 260px;
            border-top: 4px solid #3182ce; /* Pindah ke atas agar lebih rapi */
            box-shadow: 0 4px 6px rgba(0,0,0,0.02);
            transition: all 0.3s ease;
        }
        /* Efek melayang saat card di-hover */
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 12px 20px rgba(0,0,0,0.08);
            background: white;
        }
        .card h3 {
            margin-top: 0;
            color: #2b6cb0;
            font-size: 1.2em;
            margin-bottom: 12px;
        }

        /* Bagian Footer (Bawah) */
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
            transform: translateY(-2px);
            box-shadow: 0 6px 12px rgba(49, 130, 206, 0.3);
        }
        /* Warna khusus tombol github agar variatif */
        .btn-github {
            background-color: #2d3748;
            box-shadow: 0 4px 6px rgba(45, 55, 72, 0.2);
        }
        .btn-github:hover {
            background-color: #1a202c;
            box-shadow: 0 6px 12px rgba(45, 55, 72, 0.3);
        }
    </style>
</head>
<body>

    <!-- Header -->
    <header>
        <h1>Graceland Amadeus Subianto</h1>
        <p>Siswa SMA | Kreator Digital | Web Developer</p>
    </header>

    <!-- Navigasi -->
    <nav>
        <a href="#tentang">Tentang Saya</a>
        <a href="#keterampilan">Keterampilan</a>
        <a href="#pengalaman">Pengalaman</a>
        <a href="#kontak">Kontak</a>
    </nav>

    <!-- Konten Utama -->
    <div class="container">
        
        <!-- Bagian Tentang Saya -->
        <section id="tentang">
            <h2>Tentang Saya</h2>
            <p>Perkenalkan nama saya <strong>Graceland Amadeus Subianto</strong> atau biasa dipanggil Graceland. Saya merupakan siswa SMA Petra 4 Sidoarjo yang saat ini menduduki bangku kelas 11. Saya memiliki minat yang besar serta bakat di bidang teknologi, pemrograman web, dan juga strategi media sosial.</p>
        </section>

        <!-- Bagian Keterampilan -->
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

        <!-- Bagian Pengalaman & Proyek -->
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

        <!-- Bagian Kontak -->
        <section id="kontak">
            <h2>Hubungi Saya</h2>
            <p>Saya sangat terbuka untuk berdiskusi, bertukar pikiran, atau berkolaborasi dalam proyek-proyek teknologi dan kreatif lainnya. Silakan hubungi saya melalui:</p>
            <p>
                📧 Email: <strong>amadeusgraceland@gmail.com</strong><br>
                📍 Lokasi: Sidoarjo, Indonesia
            </p>
            
            <div class="sosmed-container">
                <a href="https://www.instagram.com/graceland.amadeus?igsh=MWFweHA0ZXkwdzQzZg==" class="btn-sosmed" target="_blank">Instagram</a>
                <a href="https://www.tiktok.com/@asel_web_program?_r=1&_t=ZS-96cjTGiLQmr" class="btn-sosmed" target="_blank">TikTok</a>
                <a href="https://share.google/TgwFeGnkF6gwm4PP4" class="btn-sosmed btn-github" target="_blank">GitHub / KreatifKris</a>
            </div>
        </section>

    </div>

    <!-- Footer -->
    <footer>
        <p>&copy; 2026 Graceland Amadeus. Dibuat dengan penuh dedikasi sebagai portofolio pribadi.</p>
    </footer>

</body>

