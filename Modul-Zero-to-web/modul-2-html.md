# Modul 2: HTML (Membangun Kerangka Website)

## 1. Apa itu HTML?
HTML (HyperText Markup Language) adalah bahasa markup standar yang digunakan untuk menentukan struktur sebuah halaman web[cite: 35]. Bayangkan HTML sebagai kerangka tulang dari sebuah bangunan[cite: 35]. HTML memberitahu browser mana bagian yang menjadi judul, paragraf, atau link[cite: 35].

## 2. Anatomi Elemen HTML
Kode HTML terdiri dari "Tag". Tag ini seperti label yang mengapit konten.
Sebuah elemen HTML umumnya memiliki[cite: 36]:
*   **Opening Tag:** Contoh `<p>`
*   **Content:** Isi teksnya (misal: "Halo dunia")
*   **Closing Tag:** Memiliki garis miring `</p>`

## 3. Penjelasan Tag HTML Dasar (Sintaks)
Berikut adalah tag yang paling sering digunakan saat membuat struktur website:
*   `<h1>` **hingga** `<h6>` **(Heading):** Digunakan untuk membuat teks Judul. `<h1>` adalah judul paling besar dan utama, `<h2>` untuk sub-judul, dan seterusnya mengecil hingga `<h6>`.
*   `<p>` **(Paragraph):** Digunakan untuk teks biasa atau deskripsi panjang.
*   `<img>` **(Image):** Digunakan untuk menampilkan gambar. (Tag ini unik karena tidak butuh *closing tag*).
*   `<a>` **(Anchor):** Digunakan untuk membuat tautan atau tombol link ke halaman lain.
*   **Tag Semantik** (`<header>`, `<main>`, `<section>`, `<footer>`): Tag ini seperti membuat "denah ruangan". Daripada rumah kita hanya lantai kosong, kita membaginya menjadi ruang tamu (`<header>`), ruang keluarga (`<main>`), dan halaman belakang (`<footer>`). Ini membuat kode rapi dan disukai oleh Google.

## 4. Kode Praktik: File `index.html`
Buat file `index.html` dan ketikkan struktur kerangka portofolio kita di bawah ini:

```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Portofolio Pribadi</title>
    <!-- Menghubungkan External CSS -->
    <link rel="stylesheet" href="style.css" />
</head>
<body>

<header>
    <nav class="container">
        <h2>Abidzar.</h2>
        <button id="tombol-gelap">Mode Gelap</button>
    </nav>
</header>

<main class="container">
    <section id="profil" class="kartu tata-letak-tengah">
        <!-- Pastikan nama file foto sesuai dengan yang ada di folder -->
        <img src="foto-profil.jpg" alt="Foto Profil" class="foto-profil">

        <h1 id="main-title">Halo, Saya Abidzar Dzakwan</h1>
        <p>Mahasiswa S1 Informatika yang antusias dengan pengembangan antarmuka web.</p>
        <p class="highlight">Terbuka untuk peluang kolaborasi dan magang.</p>

        <div class="wadah-tautan">
            <a href="[https://instagram.com/bizrrr_ae](https://instagram.com/bizrrr_ae)" target="_blank" class="btn-utama">Lihat Instagram saya</a>
        </div>
    </section>

    <section id="proyek" class="kartu">
        <h2>Karya Terbaru</h2>
        <ul class="daftar-proyek">
            <li><strong>Website Portofolio</strong> - Dibuat dengan HTML & CSS Murni</li>
            <li><strong>Sistem Kasir</strong> - Proyek praktikum kampus</li>
        </ul>
    </section>
</main>

<footer>
    <p>&copy; 2026 Abidzar Dzakwan Sahudi. S1 Informatika UMSurabaya.</p>
</footer>

<script src="script.js"></script>

</body>
</html>

