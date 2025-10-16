---

# 🌐 Praktikum 4: CSS Layout

**Mata Kuliah:** Pemrograman Web
**Dosen Pengampu:** Agung Nugroho, S.Kom., M.Kom.
**Nama:** Zaenal Maulana Rizki
**NIM:** 312410332
**Kelas:** TI.2A.A.4
**Universitas:** Universitas Pelita Bangsa

---

## 🎯 Tujuan Praktikum

1. Mahasiswa mampu memahami struktur dasar pembuatan layout web.
2. Mahasiswa mampu memahami konsep box element.
3. Mahasiswa mampu memahami CSS Floating.
4. Mahasiswa mampu memahami HTML5 Semantic Element.
5. Mahasiswa mampu membuat layout web sederhana.

---

## 🧰 Persiapan Awal

1. Buka **VS Code** atau text editor lainnya.
2. Buat folder baru bernama **Lab4Web**.
3. Siapkan browser untuk melihat hasil program.
4. Lakukan validasi HTML di [https://validator.w3.org](https://validator.w3.org).

---

## 🧩 Langkah-Langkah Praktikum (Halaman 36–48)

### **1. Membuat File lab4_box.html**

Buat file HTML baru bernama **lab4_box.html** dengan struktur dasar berikut:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Box Element</title>
</head>
<body>
    <header>
        <h1>Box Element</h1>
    </header>
</body>
</html>
```

---

### **2. Membuat Box Element**

Tambahkan kode berikut di dalam `<body>` untuk membuat tiga box:

```html
<section>
    <div class="div1">Div 1</div>
    <div class="div2">Div 2</div>
    <div class="div3">Div 3</div>
</section>
```

Tambahkan CSS pada bagian `<head>`:

```html
<style>
div {
    float: left;
    padding: 10px;
}
.div1 { background: red; }
.div2 { background: yellow; }
.div3 { background: green; }
</style>
```

📸 *Hasil:* Tiga kotak sejajar secara horizontal.

<img width="1208" height="295" alt="image" src="https://github.com/user-attachments/assets/bb19ff36-31b2-495c-ac0a-8ced95348db5" />


---

### **3. Mengatur Clearfix Element**

Tambahkan satu elemen div baru untuk melihat efek `clear`:

```html
<div class="div4">Div 4</div>
```

Tambahkan CSS:

```css
.div4 {
    background-color: blue;
    clear: left;
    float: none;
}
```

📸 *Hasil:* Div keempat muncul di bawah tiga box pertama.

---

### **4. Membuat Layout Web Sederhana**

Buat folder baru bernama **lab4_layout**, lalu buat dua file:

* `home.html`
* `style.css`

Isi file **home.html** dengan kode berikut:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Layout Sederhana</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="container">
        <header>
            <h1>Layout Sederhana</h1>
        </header>
        <nav>
            <a href="home.html" class="active">Home</a>
            <a href="artikel.html">Artikel</a>
            <a href="about.html">About</a>
            <a href="contact.html">Contact</a>
        </nav>
        <section id="hero">
            <h1>Hello World!</h1>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit...</p>
            <a href="#" class="btn btn-large">Learn More &raquo;</a>
        </section>
        <section id="wrapper">
            <section id="main"></section>
            <aside id="sidebar"></aside>
        </section>
        <footer>
            <p>&copy; 2025 - Universitas Pelita Bangsa</p>
        </footer>
    </div>
</body>
</html>
```

---

### **5. Menambahkan CSS Dasar (style.css)**

```css
/* Reset */
* { margin: 0; padding: 0; }

body {
    font-family: 'Open Sans', sans-serif;
    color: #5a5a5a;
}

/* Container */
#container {
    width: 980px;
    margin: 0 auto;
    box-shadow: 0 0 1em #cccccc;
}

/* Header */
header { padding: 20px; }
header h1 { color: #b5b5b5; }

/* Navigasi */
nav {
    background-color: #1f5faa;
}
nav a {
    padding: 15px 30px;
    display: inline-block;
    color: #ffffff;
    text-decoration: none;
    font-weight: bold;
}
nav a.active, nav a:hover {
    background-color: #2b83ea;
}

/* Hero Panel */
#hero {
    background-color: #e4e4e5;
    padding: 50px 20px;
    margin-bottom: 20px;
}

/* Layout */
#main { float: left; width: 640px; padding: 20px; }
#sidebar { float: left; width: 260px; padding: 20px; }

/* Footer */
footer {
    clear: both;
    background: #1d1d1d;
    color: #eee;
    padding: 20px;
}
```

📸 *Hasil:* Tampil layout dengan header, navigasi, hero panel, konten utama, sidebar, dan footer.

---

### **6. Membuat Sidebar Widget**

Tambahkan di dalam `<aside id="sidebar">`:

```html
<div class="widget-box">
  <h3 class="title">Widget Header</h3>
  <ul>
    <li><a href="#">Widget Link</a></li>
    <li><a href="#">Widget Link</a></li>
  </ul>
</div>
```

Tambahkan CSS:

```css
.widget-box { border:1px solid #eee; margin-bottom:20px; }
.widget-box .title { padding:10px; background:#428bca; color:#fff; }
.widget-box ul { list-style:none; }
.widget-box li a { padding:10px 16px; display:block; color:#333; text-decoration:none; }
.widget-box li:hover a { background-color:#eee; }
```

---

### **7. Menambahkan Elemen Artikel**

Tambahkan dalam `<section id="main">`:

```html
<article class="entry">
  <h2>First Featurette Heading</h2>
  <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="">
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit...</p>
</article>
```

Tambahkan CSS:

```css
.entry img {
  float: left;
  border-radius: 5px;
  margin-right: 15px;
}
.entry h2 { margin-bottom: 20px; }
.entry p { line-height: 25px; }
```

📸 *Hasil:* Artikel dengan gambar di sisi kiri dan teks di kanan.

---

## 🧭 Pertanyaan dan Tugas

### **1. Tambahkan Layout untuk Menu About**

Buat file `about.html` dengan isi:

```html
<section id="about">
  <h2>Tentang Saya</h2>
  <p>Saya adalah mahasiswa Informatika Universitas Pelita Bangsa...</p>
  <h3>Portfolio</h3>
  <ul>
    <li>Website Pribadi</li>
    <li>Aplikasi Kasir</li>
    <li>Desain Dashboard</li>
  </ul>
</section>
```

Tambahkan CSS:

```css
#about { padding: 20px; line-height: 25px; }
#about h2 { color: #1f5faa; }
```

📸 *Hasil:* Halaman About berisi deskripsi dan portfolio sederhana.

---

### **2. Tambahkan Layout untuk Menu Contact**

Buat file `contact.html` dengan isi:

```html
<section id="contact">
  <h2>Hubungi Saya</h2>
  <form>
    <p><label>Nama:</label><br><input type="text" name="nama"></p>
    <p><label>Email:</label><br><input type="email" name="email"></p>
    <p><label>Pesan:</label><br><textarea name="message" rows="5"></textarea></p>
    <p><input type="submit" value="Kirim"></p>
  </form>
</section>
```

Tambahkan CSS:

```css
form input, form textarea {
  width: 100%;
  padding: 8px;
  margin: 5px 0;
  border: 1px solid #ccc;
  border-radius: 5px;
}
input[type="submit"] {
  background-color: #1f5faa;
  color: #fff;
  border: none;
  padding: 10px 20px;
  cursor: pointer;
}
```

📸 *Hasil:* Halaman Contact berisi form input nama, email, dan pesan.

---

## 🧾 Laporan Praktikum

1. Buat repository GitHub dengan nama **Lab4Web**.
2. Kerjakan semua latihan sesuai urutan di atas.
3. Screenshot setiap perubahan hasil kode.
4. Buat file **README.md** (dokumen ini) dan jelaskan setiap langkah disertai screenshot.
5. Lakukan **commit & push** ke repository masing-masing.
6. Kirim **URL repository GitHub** ke e-learning **Ecampus Universitas Pelita Bangsa**.

---

## ✅ Kesimpulan

Dalam praktikum ini telah dipelajari:

* Struktur layout dasar menggunakan **HTML5 Semantic Element**.
* Konsep **Box Element**, **Float**, dan **Clearfix**.
* Cara membuat layout web sederhana dengan navigasi, hero panel, sidebar, dan footer.
* Implementasi tambahan halaman **About** dan **Contact** sesuai instruksi tugas.

---
