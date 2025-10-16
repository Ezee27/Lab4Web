Oke 👍 berikut versi **README.md lengkap, halaman 36–48 + Pertanyaan & Tugas + Laporan Praktikum**,
yang **sudah disertai penjelasan di setiap bagian kodenya** agar mudah kamu pahami dan cocok untuk laporan GitHub.

---

# 🌐 Praktikum 4: CSS Layout

**Mata Kuliah:** Pemrograman Web
**Dosen Pengampu:** Agung Nugroho, S.Kom., M.Kom.
**Nama:** [Nama Lengkap Anda]
**NIM:** [Nomor Induk Mahasiswa]
**Kelas:** TI.2A.A.4
**Universitas:** Universitas Pelita Bangsa
**Repository:** `Lab4Web`

---

## 🎯 Tujuan Praktikum

1. Mahasiswa mampu memahami struktur dasar pembuatan layout web.
2. Mahasiswa mampu memahami konsep box element dan CSS Float.
3. Mahasiswa mampu memahami HTML5 Semantic Element.
4. Mahasiswa mampu membuat layout web sederhana.

---

## 🧰 Persiapan Awal

1. Buka **VS Code** atau text editor lainnya.
2. Buat folder baru bernama **Lab4Web**.
3. Siapkan browser untuk menampilkan hasil.
4. Validasi kode HTML di [https://validator.w3.org](https://validator.w3.org).

---

## 🧩 Langkah-Langkah Praktikum

### **1. Membuat File lab4_box.html**

Pertama kita buat struktur dasar HTML.

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

📝 **Penjelasan:**

* `<!DOCTYPE html>` → Menandakan bahwa dokumen menggunakan HTML5.
* `<head>` → Berisi informasi meta dan judul halaman.
* `<body>` → Menampilkan konten yang akan dilihat pengguna.
* `<header>` → Elemen semantik untuk bagian atas halaman (judul website).

---

### **2. Membuat Box Element**

Sekarang kita tambahkan tiga kotak (box) menggunakan tag `<div>`.

```html
<section> 
    <div class="div1">Div 1</div> 
    <div class="div2">Div 2</div> 
    <div class="div3">Div 3</div>       
</section>
```

📝 **Penjelasan:**

* `<section>` → Untuk mengelompokkan konten agar lebih terstruktur.
* Tiga `<div>` mewakili tiga kotak berbeda yang akan diberi warna dan posisi dengan CSS.

Tambahkan CSS di dalam `<head>` untuk mengatur tampilannya:

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

📝 **Penjelasan CSS:**

* `float: left;` → Membuat elemen sejajar ke kiri.
* `padding` → Memberi jarak antara konten dan tepi box.
* `.div1`, `.div2`, `.div3` → Memberi warna berbeda pada tiap kotak.

📸 **Hasil:** Tiga kotak sejajar secara horizontal berwarna merah, kuning, dan hijau.

---

### **3. Menambahkan Clearfix**

Sekarang kita tambahkan kotak keempat dan gunakan properti `clear` agar tampil di bawah.

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

📝 **Penjelasan:**

* `clear: left;` → Menghapus efek float dari elemen sebelumnya agar elemen baru muncul di bawahnya.
* `float: none;` → Menonaktifkan efek melayang.

📸 **Hasil:** Kotak keempat berwarna biru muncul di bawah tiga kotak lainnya.

---

### **4. Membuat Layout Web Sederhana**

Sekarang kita akan membuat halaman website lengkap dengan header, navigasi, konten, dan footer.

Buat folder baru bernama `lab4_layout`, kemudian buat file **home.html** dan **style.css**.

#### File: `home.html`

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
    <header><h1>Layout Sederhana</h1></header>

    <nav>
      <a href="home.html" class="active">Home</a>
      <a href="artikel.html">Artikel</a>
      <a href="about.html">About</a>
      <a href="contact.html">Contact</a>
    </nav>

    <section id="hero">
      <h1>Hello World!</h1>
      <p>Ini adalah contoh layout web sederhana menggunakan HTML dan CSS.</p>
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

📝 **Penjelasan:**

* `<nav>` → Tempat menu navigasi antar halaman.
* `<section id="hero">` → Bagian utama (hero panel).
* `<section id="wrapper">` → Wadah untuk main content dan sidebar.
* `<footer>` → Bagian bawah halaman berisi hak cipta.

---

#### File: `style.css`

```css
/* Reset CSS */
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
  color: #fff;
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

/* Layout utama */
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

📝 **Penjelasan:**

* `#container` → Mengatur ukuran layout utama (980px).
* `nav a` → Mengatur tampilan menu link.
* `#hero` → Memberi warna latar dan padding untuk bagian hero.
* `float` → Mengatur posisi konten dan sidebar sejajar.
* `footer` → Dibuat selalu di bawah dengan `clear: both`.

📸 **Hasil:** Website sederhana dengan header, menu, hero panel, main, sidebar, dan footer.

---

### **5. Membuat Sidebar Widget**

Tambahkan pada bagian `<aside>`:

```html
<aside id="sidebar">
  <div class="widget-box">
    <h3 class="title">Widget Header</h3>
    <ul>
      <li><a href="#">Widget Link 1</a></li>
      <li><a href="#">Widget Link 2</a></li>
      <li><a href="#">Widget Link 3</a></li>
    </ul>
  </div>
</aside>
```

Tambahkan CSS:

```css
.widget-box {
  border: 1px solid #eee;
  margin-bottom: 20px;
}
.widget-box .title {
  padding: 10px 16px;
  background-color: #428bca;
  color: #fff;
}
.widget-box ul { list-style-type: none; }
.widget-box li a {
  padding: 10px 16px;
  color: #333;
  display: block;
  text-decoration: none;
}
.widget-box li:hover a { background-color: #eee; }
```

📝 **Penjelasan:**

* Widget dibuat dengan `<div>` agar mudah diatur per box.
* CSS memberikan warna biru pada header widget dan efek hover pada link.

---

### **6. Menambahkan Artikel di Main Content**

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

📝 **Penjelasan:**

* `float: left` menempatkan gambar di kiri teks.
* `border-radius` membuat gambar sudutnya melengkung.
* `line-height` mengatur jarak antarbaris teks.

---

## 🧭 Pertanyaan dan Tugas

### **1. Layout Menu About**

Buat file **about.html** berisi deskripsi diri & portfolio.

```html
<section id="about">
  <h2>Tentang Saya</h2>
  <p>Saya adalah mahasiswa Informatika Universitas Pelita Bangsa. Saya tertarik di bidang Web Development dan UI/UX Design.</p>

  <h3>Portfolio</h3>
  <ul>
    <li>Website Profil</li>
    <li>Aplikasi Kasir Sederhana</li>
    <li>Desain Dashboard Admin</li>
  </ul>
</section>
```

Tambahkan CSS:

```css
#about {
  padding: 20px;
  line-height: 25px;
}
#about h2 {
  color: #1f5faa;
  margin-bottom: 10px;
}
```

📝 **Penjelasan:**

* Halaman ini menampilkan biodata singkat dan daftar portfolio.
* CSS memberikan jarak dan warna biru pada judul bagian.

---

### **2. Layout Menu Contact**

Buat file **contact.html** berisi form kontak.

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

📝 **Penjelasan:**

* `form` digunakan untuk menerima input pengguna.
* Input terdiri dari nama, email, dan pesan.
* Tombol kirim diberi warna biru dan efek pointer saat diarahkan kursor.

📸 **Hasil:** Form tampil rapi dengan border lembut dan tombol kirim biru.

---

## 🧾 Laporan Praktikum

1. Buat repository GitHub bernama **Lab4Web**.
2. Kerjakan semua latihan sesuai urutan di atas.
3. Screenshot setiap hasil perubahan dan tampilannya.
4. Buat file **README.md** (dokumen ini) berisi penjelasan langkah dan screenshot.
5. Lakukan **commit dan push** ke repository GitHub.
6. Kirim **URL repository GitHub** di **Ecampus Universitas Pelita Bangsa**.

---

## ✅ Kesimpulan

Dalam praktikum ini, telah dipelajari:

* Struktur dasar layout menggunakan HTML5 Semantic Elements.
* Penggunaan CSS Float, Box Model, dan Clearfix.
* Pembuatan halaman web sederhana dengan bagian header, navigasi, hero panel, sidebar, dan footer.
* Implementasi halaman tambahan **About** dan **Contact** dengan desain rapi dan form input.

---

Apakah kamu mau saya bantu **ubah ini langsung jadi file `README.md` siap upload ke GitHub**, dengan nama, NIM, dan kelas kamu diisi otomatis juga?
