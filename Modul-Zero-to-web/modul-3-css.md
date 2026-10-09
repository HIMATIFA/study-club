# Modul 3: CSS (Mempercantik Tampilan Website)

## 1. Apa itu CSS?
CSS (Cascading Style Sheets) adalah bahasa yang digunakan untuk mengatur tampilan dokumen yang ditulis dalam HTML[cite: 39]. Jika HTML adalah kerangkanya, maka CSS adalah pakaian, cat, dan dekorasinya[cite: 39]. CSS memungkinkan modifikasi warna, font, ukuran, hingga posisi elemen di layar[cite: 39].

## 2. Bagaimana Cara Menulis CSS?
Sintaks CSS sangat sederhana dan terdiri dari tiga bagian utama:
```css
selector {
    property: value;
}
```

Selector: Target elemen HTML yang ingin diubah gayanya.   
Property: Aspek gaya yang ingin diubah (misal: warna, ukuran font).   
Value: Nilai dari properti tersebut[cite: 40].


## 3. Mengenal Pemilih (Selector) CSS
Terdapat 3 cara utama memilih elemen di HTML untuk dihias oleh CSS:
* **Element Selector:** Memilih elemen berdasarkan nama tag HTML secara langsung (misal `h1 { text-transform: uppercase; }`).
* **Class Selector:** Memilih elemen berdasarkan atribut class menggunakan tanda titik (`.`) di depan nama class. Dipakai jika kita ingin memberi gaya yang sama pada banyak elemen.
* **ID Selector:** Memilih satu elemen unik dengan atribut id tertentu menggunakan tanda pagar (`#`). *Catatan: ID sebaiknya unik di satu halaman, sedangkan class bisa dipakai berulang kali.*

## 4. Penjelasan Sintaks CSS Penting
Pada praktik kali ini, kita menggunakan beberapa properti CSS yang sangat sering dipakai di dunia industri pembuatan web:

**1. Tata Letak (Layouting)**
* `display: flex;`: Mengaktifkan mode *Flexbox*. Ini adalah "sihir" CSS modern untuk menyejajarkan elemen (seperti menu navigasi) ke samping atau ke bawah dengan sangat mudah.
* `justify-content` & `align-items`: Pasangan dari Flexbox. Berfungsi untuk meratakan posisi elemen, misalnya membuatnya pas di tengah-tengah kotak atau menyebar ke ujung kiri dan kanan.
* `max-width: 700px;` & `margin: 0 auto;`: Kombinasi sakti untuk membatasi lebar maksimal konten dan memposisikannya tepat di tengah layar laptop, agar website tidak melebar berantakan.

**2. Visual & Estetika (Styling)**
* `background-color` & `color`: `background-color` untuk mewarnai latar belakang, sedangkan `color` khusus untuk mewarnai teks.
* `border-radius`: Membuat sudut elemen tidak kaku. Diisi angka kecil (misal `8px`) untuk sudut melengkung, atau `50%` untuk mengubah gambar kotak menjadi bulat sempurna.
* `box-shadow`: Memberikan bayangan halus di belakang elemen (seperti kartu atau foto) agar terlihat menonjol dan memiliki efek 3D (tidak datar).

**3. Konten & Gambar**
* `text-decoration: none;`: Menghilangkan garis bawah warna biru yang secara *default* selalu muncul pada tag link `<a>`.
* `object-fit: cover;`: Sangat penting untuk gambar! Properti ini mencegah foto profil Anda menjadi gepeng atau melar ketika dipaksa masuk ke ukuran kotak (misalnya 150x150px).

**4. Interaksi & Animasi**
* `:hover`: Efek transisi (*pseudo-class*) yang mengubah gaya suatu elemen saat kursor *mouse* diarahkan ke atasnya (contoh: tombol berubah warna saat disorot).
* `transition`: Membuat setiap perubahan visual—seperti animasi saat tombol disorot atau saat web berubah ke *Dark Mode*—terjadi secara halus dan tidak mendadak.

## 5. Kode Praktik: File `style.css`
Buat file `style.css` terpisah dan ketikkan kode berikut untuk merapikan struktur HTML portofolio:

````
// style.css
* {
margin: 0;
padding: 0;
box-sizing: border-box;
}

body {
font-family: system-ui, -apple-system, sans-serif;
background-color: #f8fafc;
color: #1e293b;
line-height: 1.6;
transition: 0.3s;
}

.container {
max-width: 700px;
margin: 0 auto;   
padding: 0 20px;
}

header {
background-color: #ffffff;
border-bottom: 1px solid #e2e8f0;
padding: 15px 0;
}

nav {
display: flex;
justify-content: space-between;
align-items: center;
}

#tombol-gelap {
background-color: #f1f5f9;
border: none;
padding: 8px 16px;
border-radius: 20px;
font-weight: 600;
cursor: pointer;
transition: 0.2s;
}

#tombol-gelap:hover {
background-color: #e2e8f0;
}

main {
padding-top: 30px;
}

.kartu {
background-color: #ffffff;
border: 1px solid #e2e8f0;
border-radius: 16px;
padding: 40px 30px;
margin-bottom: 25px;
box-shadow: 0 4px 6px rgba(0,0,0,0.02);
}

.tata-letak-tengah {
text-align: center;
}

/* Gambar Profil Bulat Sempurna */
.foto-profil {
width: 150px;
height: 150px;
border-radius: 50%;
object-fit: cover;  
border: 4px solid #ffffff;
box-shadow: 0 4px 10px rgba(0,0,0,0.1);
margin-bottom: 20px;
}

#main-title {
color: #0f766e;
font-size: 26px;
margin-bottom: 10px;
}

.highlight {
background-color: #ccfbf1;
color: #115e59;
font-weight: 600;
display: inline-block;
padding: 6px 16px;
border-radius: 20px;
font-size: 14px;
margin-bottom: 15px;
}

.wadah-tautan {
margin-top: 20px;
}

.btn-utama {
display: inline-block;
background-color: #0f766e;
color: #ffffff;
text-decoration: none;
padding: 10px 24px;
border-radius: 8px;
font-weight: 600;
transition: 0.3s;
}

.btn-utama:hover {
background-color: #115e59;
transform: translateY(-2px);
}

.daftar-proyek {
list-style: none;
margin-top: 15px;
}

.daftar-proyek li {
padding: 12px 0;
border-bottom: 1px dashed #e2e8f0;
}

footer {
text-align: center;
color: #64748b;
font-size: 14px;
padding: 20px 0 40px 0;
}

.mode-gelap {
background-color: #0f172a;
color: #f8fafc;
}

.mode-gelap header,
.mode-gelap .kartu {
background-color: #1e293b;
border-color: #334155;
}

.mode-gelap #tombol-gelap {
background-color: #334155;
color: white;
}

.mode-gelap .foto-profil {
border-color: #334155;
}
````
