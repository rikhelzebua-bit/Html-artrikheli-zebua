<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>KopiKita Cafe - Rasakan Kenikmatan Setiap Tegukan</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        :root {
            --warna-utama: #8B5A2B;
            --warna-kedua: #F5DEB3;
            --warna-tua: #3C2A21;
            --warna-putih: #FFFFFF;
            --warna-abu: #F8F8F8;
        }

        header {
            background-image: url('https://images.unsplash.com/photo-1504753793650-d4a2b783c15e?ixlib=rb-4.0.3&auto=format&fit=crop&w=1470&q=80');
            background-size: cover;
            background-position: center;
            color: var(--warna-putih);
            text-align: center;
            padding: 8rem 2rem;
            position: relative;
        }

        header::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5);
        }

        header > * {
            position: relative;
            z-index: 1;
        }

        nav {
            background-color: var(--warna-tua);
            padding: 1rem 2rem;
            position: sticky;
            top: 0;
            z-index: 10;
        }

        nav ul {
            list-style: none;
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
            justify-content: center;
        }

        nav a {
            color: var(--warna-putih);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }

        nav a:hover {
            color: var(--warna-kedua);
        }

        .section {
            padding: 4rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .judul-section {
            color: var(--warna-utama);
            text-align: center;
            margin-bottom: 3rem;
            font-size: 2rem;
        }

        /* Menu Kopi */
        .menu-kopi {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }

        .card-kopi {
            background-color: var(--warna-abu);
            border-radius: 10px;
            padding: 1.5rem;
            text-align: center;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }

        .card-kopi:hover {
            transform: translateY(-5px);
        }

        .card-kopi img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            border-radius: 8px;
            margin-bottom: 1rem;
        }

        .nama-kopi {
            color: var(--warna-tua);
            font-size: 1.2rem;
            font-weight: bold;
        }

        .deskripsi-kopi {
            color: #666;
            margin: 0.5rem 0;
            font-size: 0.9rem;
        }

        .harga-kopi {
            color: var(--warna-utama);
            font-size: 1.1rem;
            font-weight: bold;
            margin-top: 1rem;
        }

        /* Lokasi */
        .lokasi {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
            align-items: center;
            justify-content: center;
        }

        .lokasi-map {
            flex: 1 1 400px;
            height: 300px;
            border-radius: 10px;
            overflow: hidden;
            border: 2px solid var(--warna-kedua);
        }

        .lokasi-info {
            flex: 1 1 300px;
        }

        .lokasi-info h3 {
            color: var(--warna-utama);
            margin-bottom: 1rem;
        }

        .lokasi-info p {
            margin: 0.5rem 0;
            line-height: 1.6;
        }

        /* Footer */
        footer {
            background-color: var(--warna-tua);
            color: var(--warna-putih);
            text-align: center;
            padding: 2rem;
        }

        /* Tombol Scroll */
        #tombol-scroll {
            position: fixed;
            bottom: 2rem;
            right: 2rem;
            background-color: var(--warna-utama);
            color: var(--warna-putih);
            border: none;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            cursor: pointer;
            display: none;
            transition: background-color 0.3s;
        }

        #tombol-scroll:hover {
            background-color: var(--warna-tua);
        }

        @media (max-width: 576px) {
            header {
                padding: 5rem 1rem;
            }

            .judul-section {
                font-size: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <!-- Navigasi -->
    <nav>
        <ul>
            <li><a href="#beranda">Beranda</a></li>
            <li><a href="#menu">Menu Kopi</a></li>
            <li><a href="#lokasi">Lokasi</a></li>
            <li><a href="#kontak">Kontak</a></li>
        </ul>
    </nav>

    <!-- Header/Beranda -->
    <header id="beranda">
        <h1>KopiKita Cafe</h1>
        <p style="margin-top: 1rem; font-size: 1.2rem;">Kualitas Kopi Premium dari Petani Lokal Sumatera Utara</p>
    </header>

    <!-- Menu Kopi -->
    <section class="section" id="menu">
        <h2 class="judul-section">Menu Kopi Kami</h2>
        <div class="menu-kopi">
            <!-- Card Kopi 1 -->
            <div class="card-kopi">
                <img src="https://images.unsplash.com/photo-1542909168-82c3e7fdca5c?ixlib=rb-4.0.3&auto=format&fit=crop&w=1470&q=80" alt="Espresso">
                <div class="nama-kopi">Espresso</div>
                <div class="deskripsi-kopi">Kopi pekat yang dibuat dengan menekan air panas melalui biji kopi yang sudah digiling halus</div>
                <div class="harga-kopi">Rp 15.000</div>
            </div>

            <!-- Card Kopi 2 -->
            <div class="card-kopi">
                <img src="https://images.unsplash.com/photo-1534197442473-841ab6471d6b?ixlib=rb-4.0.3&auto=format&fit=crop&w=1470&q=80" alt="Cappuccino">
                <div class="nama-kopi">Cappuccino</div>
                <div class="deskripsi-kopi">Campuran espresso, susu panas, dan busa susu yang banyak dengan rasio seimbang</div>
                <div class="harga-kopi">Rp 20.000</div>
            </div>

            <!-- Card Kopi 3 -->
            <div class="card-kopi">
                <img src="https://images.unsplash.com/photo-1576673210558-581792852116?ixlib=rb-4.0.3&auto=format&fit=crop&w=1470&q=80" alt="Latte">
                <div class="nama-kopi">Latte</div>
                <div class="deskripsi-kopi">Espresso dengan tambahan susu panas dan sedikit busa susu di atasnya</div>
                <div class="harga-kopi">Rp 22.000</div>
            </div>

            <!-- Card Kopi 4 -->
            <div class="card-kopi">
                <img src="https://images.unsplash.com/photo-1585088762211-7a40166e0885?ixlib=rb-4.0.3&auto=format&fit=crop&w=1470&q=80" alt="Americano">
                <div class="nama-kopi">Americano</div>
                <div class="deskripsi-kopi">Espresso yang dicampur dengan air panas untuk menghasilkan rasa yang lebih ringan</div>
                <div class="harga-kopi">Rp 18.000</div>
            </div>

            <!-- Card Kopi 5 -->
            <div class="card-kopi">
                <img src="https://images.unsplash.com/photo-1594820289599-9f32a4f98953?ixlib=rb-4.0.3&auto=format&fit=crop&w=1470&q=80" alt="Mocha">
                <div class="nama-kopi">Mocha</div>
                <div class="deskripsi-kopi">Kombinasi espresso, susu panas, sirup coklat, dan busa susu dengan taburan bubuk coklat</div>
                <div class="harga-kopi">Rp 25.000</div>
            </div>

            <!-- Card Kopi 6 -->
            <div class="card-kopi">
                <img src="https://images.unsplash.com/photo-1614349255597-8a54abfd0948?ixlib=rb-4.0.3&auto=format&fit=crop&w=1470&q=80" alt="Kopi Tubruk">
                <div class="nama-kopi">Kopi Tubruk</div>
                <div class="deskripsi-kopi">Kopi tradisional Indonesia yang dibuat dengan menyeduh biji kopi giling kasar bersama gula dalam air panas</div>
                <div class="harga-kopi">Rp 17.000</div>
            </div>
        </div>
    </section>

    <!-- Lokasi -->
    <section class="section" id="lokasi">
        <h2 class="judul-section">Temukan Kami Di Sini</h2>
        <div class="lokasi">
            <div class="lokasi-map">
                <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3989.772608533751!2d98.6666373147613!3d3.587887197448373!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x30313174ffb25b47%3A0x4732136f16068393!2sMedan%20City%2C%20North%20Sumatra!5e0!3m2!1sen!2sid!4v1738065200000!5m2!1sen!2sid" width="100%" height="100%" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
            </div>
            <div class="lokasi-info">
                <h3>KopiKita Cafe Medan</h3>
                <p><strong>Alamat:</strong> Jl. dahanatabaloho No. 123, Kecamatan Gunungsitoli Barat, Gununungsitoli, Sumatera Utara</p>
                <p><strong>Jam Buka:</strong></p>
                <p>Senin - Jumat: 07.00 WIB - 22.00 WIB</p>
                <p>Sabtu - Minggu & Hari Libur: 08.00 WIB - 23.00 WIB</p>
                <p><strong>No. Telepon:</strong> 082250626994</p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer id="kontak">
        <p>&copy; 2026 KopiKita Cafe. Semua Hak Dilindungi.</p>
        <p style="margin-top: 0.5rem;">Ikuti Kami: Instagram @kopikitacafe_rikhel | WhatsApp 082250626994</p>
    </footer>

    <!-- Tombol Scroll ke Atas -->
    <button id="tombol-scroll" onclick="scrollKeAtas()">↑</button>

    <script>
        // Tombol Scroll ke Atas
        const tombolScroll = document.getElementById('tombol-scroll');
        window.onscroll = function() {
            if (document.body.scrollTop > 300 || document.documentElement.scrollTop > 300) {
                tombolScroll.style.display = "block";
            } else {
                tombolScroll.style.display = "none";
            }
        };

        function scrollKeAtas() {
            document.body.scrollTop = 0;
            document.documentElement.scrollTop = 0;
        }

        // Smooth Scroll untuk Navigasi
        document.querySelectorAll('nav a').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
