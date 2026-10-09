# Modul 4: JavaScript & DOM (Memberikan Nyawa pada Web)

## 1. Apa itu JavaScript?
JavaScript adalah bahasa pemrograman yang digunakan untuk membuat halaman web menjadi lebih hidup, interaktif, dan dinamis[cite: 49]. Dalam praktiknya, JavaScript berfungsi memberikan perilaku (*behavior*) dan logika pada halaman web[cite: 50].

> **💡 Analogi Kelistrikan:**
> Ibarat sistem kelistrikan pada sebuah rumah, JavaScript bertindak sebagai saklar penghubung yang menghidupkan fitur-fitur seperti *pop-up alert*, validasi formulir, hingga pergantian tema seperti fitur *Dark Mode*[cite: 50].

## 2. Berkenalan dengan DOM (Jembatan HTML & JS)
**Apa itu DOM?**
Document Object Model (DOM) adalah jembatan atau antarmuka pemrograman (API) yang menghubungkan antara dokumen HTML dengan JavaScript[cite: 53]. DOM bekerja dengan cara merepresentasikan seluruh halaman web menjadi sebuah struktur objek, sehingga JavaScript memiliki akses penuh untuk membaca, mengubah, menambah, atau menghapus elemen HTML apa pun yang ada di layar[cite: 53].

> **💡 Analogi Boneka Wayang (Marionette):**
> Bayangkan DOM seperti **tali penggerak pada boneka wayang**[cite: 54]. Elemen HTML (tombol, teks) adalah wujud fisik bonekanya yang diam dan kaku[cite: 54]. JavaScript adalah sang dalang yang bertugas memberikan perintah gerakan[cite: 54]. Nah, DOM adalah "tali-tali" yang menghubungkan tangan dalang ke boneka tersebut[cite: 51, 54].

## 3. Formula 3 Langkah JavaScript
Interaksi JavaScript pada web selalu bekerja melalui tiga langkah utama ini[cite: 52]:
* **Tangkap Elemennya (DOM Selection):** Mencari elemen HTML yang mau digerakkan (contoh: `document.getElementById`).
* **Dengarkan Aksinya (Event Listener):** Memasang "telinga" untuk menunggu aksi pengguna, seperti tombol yang diklik (contoh: `addEventListener`).
* **Berikan Reaksinya (Manipulasi DOM):** Mengeksekusi perubahan tampilan secara *real-time* di layar (contoh: `classList.toggle`).

## 4. Kode Praktik: File `script.js`
Buat file `script.js` di dalam folder yang sama, lalu ketikkan "Formula 3 Langkah" berikut untuk membuat tombol saklar *Dark Mode* pada portofolio Anda:

```javascript
// LANGKAH 1: Tangkap Elemen HTML (DOM Selection)
// Kita mencari elemen tombol berdasarkan ID "tombol-gelap" yang ada di HTML
const tombol = document.getElementById("tombol-gelap");

// LANGKAH 2: Dengarkan Aksi Pengguna (Event Listener)
// Kita pasang pendengar, jadi saat tombol di-"click", fungsi di dalamnya akan berjalan
tombol.addEventListener("click", function() {
    
    // LANGKAH 3: Berikan Reaksi (Manipulasi DOM)
    // .toggle bekerja persis seperti saklar lampu. 
    // Menyalakan class 'mode-gelap' pada body jika belum ada, dan mematikannya jika sudah ada.
    document.body.classList.toggle("mode-gelap");
    
});
