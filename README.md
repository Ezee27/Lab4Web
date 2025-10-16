---

# 🌐 Praktikum 4: CSS Layout

---

**Mata Kuliah:** Pemrograman Web**
**Dosen Pengampu:** Agung Nugroho, S.Kom., M.Kom.**
**Nama:** [Nama Kamu]
**NIM:** [NIM Kamu]
**Kelas:** TI.2A.A.4
**Universitas:** Universitas Pelita Bangsa

---

## 🎯 Tujuan Praktikum

1. Mahasiswa mampu memahami struktur dasar pembuatan Layout.
2. Mahasiswa mampu memahami konsep Box Element.
3. Mahasiswa mampu memahami CSS Floating.
4. Mahasiswa mampu memahami HTML5 Semantic Element.
5. Mahasiswa mampu membuat Layout Web Sederhana.

---

## ⚙️ Instruksi Praktikum

1. Persiapkan text editor (contoh: **VSCode**)
2. Buat folder baru dengan nama **Lab4Web**
3. Ikuti langkah-langkah praktikum berikut ini secara berurutan
4. Lakukan validasi HTML di [https://validator.w3.org](https://validator.w3.org)

---

## 🧩 Langkah-Langkah Praktikum

### **1. Persiapan Membuat Dokumen HTML**

Buat file baru bernama **lab4_box.html** dengan kode berikut:

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

* Baris `<!DOCTYPE html>` menandakan dokumen HTML5.
* `<meta charset="UTF-8">` untuk mendukung karakter Unicode.
* `<header>` berisi judul halaman “Box Element”.

---

### **2. Membuat Box Element**

Tambahkan kode berikut setelah tag `<header>` untuk membuat 3 kotak:

```html
<section> 
    <div class="div1">Div 1</div> 
    <div class="div2">Div 2</div> 
    <div class="div3">Div 3</div>       
</section>
```

Kemudian tambahkan CSS di bagian `<head>` seperti berikut:

```html
<style> 
    div { 
        float:left; 
        padding: 10px;  
    } 
    .div1 { 
        background: red; 
    } 
    .div2 { 
        background: yellow; 
    } 
    .div3 { 
        background: green; 
    } 
</style>
```

📝 **Penjelasan:**

* `float:left;` → Menyusun semua div secara horizontal ke kiri.
* `padding:10px;` → Memberikan jarak di dalam kotak.
* `.div1`, `.div2`, `.div3` → Memberi warna yang berbeda pada setiap kotak.

📸 **Hasil:** Akan tampil tiga kotak sejajar berwarna merah, kuning, dan hijau.

<img width="755" height="219" alt="image" src="https://github.com/user-attachments/assets/38e1fa5c-5db8-4427-a2df-236bd73ea8e4" />

---

### **3. Mengatur Clearfix Element**

Tambahkan satu elemen lagi di bawah tiga kotak tersebut:

```html
<section> 
    <div class="div1">Div 1</div> 
    <div class="div2">Div 2</div> 
    <div class="div3">Div 3</div>   
    <div class="div4">Div 4</div>     
</section>
```

Kemudian tambahkan CSS berikut:

```css
.div4 { 
    background-color: blue; 
    clear: left; 
    float: none; 
}
```

📝 **Penjelasan:**

* `clear:left;` digunakan agar elemen `div4` tidak sejajar dengan kotak lainnya, tapi turun ke bawah.
* `float:none;` menonaktifkan efek “mengapung”.

📸 **Hasil:** Div 4 muncul di bawah tiga box lainnya berwarna biru.

<img width="1208" height="295" alt="image" src="https://github.com/user-attachments/assets/bb19ff36-31b2-495c-ac0a-8ced95348db5" />

---

### **4. Membuat Layout Web Sederhana**

Buat folder baru dengan nama **lab4_layout**, kemudian buat file baru **home.html** dan **style.css**.

Isi file **home.html** sebagai berikut:

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
            <a href="kontak.html">Kontak</a> 
        </nav> 
        <section id="hero"> 
            <h1>Hello World!</h1> 
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit...</p> 
            <a href="#" class="btn btn-large">Learn more &raquo;</a> 
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

* `#container` → pembungkus utama seluruh layout.
* `<nav>` → menu navigasi antar halaman.
* `<section id="hero">` → panel utama berisi teks dan tombol.
* `<section id="wrapper">` → area isi dan sidebar.
* `<footer>` → area bawah halaman.

---

### **5. Menambahkan CSS Layout**

Isi file **style.css** dengan kode berikut:

```css
/* import google font */ 
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@300;400;600;700&display=swap');

/* Reset CSS */ 
* { 
    margin: 0; 
    padding: 0; 
} 

body { 
    line-height:1; 
    font-size:100%; 
    font-family:'Open Sans', sans-serif; 
    color:#5a5a5a; 
} 

#container { 
    width: 980px; 
    margin: 0 auto; 
    box-shadow: 0 0 1em #cccccc; 
} 

/* header */ 
header { 
    padding: 20px; 
} 
header h1 { 
    margin: 20px 10px; 
    color: #b5b5b5; 
} 

/* navigasi */ 
nav { 
    display: block; 
    background-color: #1f5faa; 
} 
nav a { 
    padding: 15px 30px; 
    display: inline-block; 
    color: #ffffff; 
    font-size: 14px; 
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
#hero h1 { 
    margin-bottom: 20px; 
    font-size: 35px; 
} 
#hero p { 
    margin-bottom: 20px; 
    font-size: 18px; 
    line-height: 25px; 
}

/* main content dan sidebar */ 
#wrapper { margin: 0; } 
#main { float: left; width: 640px; padding: 20px; } 
#sidebar { float: left; width: 260px; padding: 20px; }

/* widget */ 
.widget-box { border:1px solid #eee; margin-bottom:20px; } 
.widget-box .title { padding:10px 16px; background-color:#428bca; color:#fff; } 
.widget-box ul { list-style-type:none; } 
.widget-box li { border-bottom:1px solid #eee; } 
.widget-box li a { padding:10px 16px; color:#333; display:block; text-decoration:none; } 
.widget-box li:hover a { background-color:#eee; } 
.widget-box p { padding:15px; line-height:25px; }

/* footer */ 
footer { 
    clear:both; 
    background-color:#1d1d1d; 
    padding:20px; 
    color:#eee; 
}
```

📝 **Penjelasan:**

* Mengatur tampilan header, navigasi, hero panel, konten utama, sidebar, dan footer.
* Menggunakan `float` untuk membagi layout dua kolom.
* Menggunakan `clear:both` di footer agar selalu di bawah.

📸 **Hasil:** Tampilan layout web sederhana dengan menu dan konten.

---

### **6. Menambahkan Elemen di Main Content**

Tambahkan di dalam `<section id="main">`:

```html
<div class="row"> 
    <div class="box"> 
        <img src="https://dummyimage.com/120/db7d25/fff.png" alt="" class="image-circle"> 
        <h3>Heading</h3> 
        <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p> 
        <a href="#" class="btn btn-default">View detail</a> 
    </div> 
</div>
```

📝 **Penjelasan:**

* `.row` untuk menampung beberapa kotak.
* `.box` berisi gambar, judul, teks, dan tombol kecil.
* `.image-circle` digunakan untuk membuat gambar bulat.

Tambahkan CSS:

```css
.box { display:block; float:left; width:33.3%; padding:0 10px; text-align:center; } 
.image-circle { border-radius:50%; }
```

---

### **7. Menambahkan Content Artikel**

Tambahkan HTML berikut:

```html
<hr class="divider" /> 
<article class="entry"> 
    <h2>First featurette heading.</h2> 
    <img src="https://dummyimage.com/150/7b8a70/fff.png" alt=""> 
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit...</p> 
</article>
```

Dan tambahkan CSS:

```css
.divider { border:0; border-top:1px solid #eeeeee; margin:40px 0; } 
.entry img { float:left; border-radius:5px; margin-right:15px; } 
.entry h2 { margin-bottom:20px; } 
.entry p { line-height:25px; }
```

📸 **Hasil:** Artikel dengan gambar di kiri dan teks di kanan.

---

## 🧭 Pertanyaan dan Tugas

### **1. Tambahkan Layout untuk Menu About**

👉 Buat file baru `about.html` berisi:

```html
<section id="about">
  <h2>Tentang Saya</h2>
  <p>Saya mahasiswa Teknik Informatika Universitas Pelita Bangsa...</p>
  <h3>Portfolio</h3>
  <ul>
    <li>Website Profil</li>
    <li>Aplikasi Kasir</li>
    <li>Desain Dashboard</li>
  </ul>
</section>
```

### **2. Tambahkan Layout untuk Menu Contact**

👉 Buat file `contact.html` berisi form:

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

---

## 📑 Laporan Praktikum

1. Buat repository GitHub bernama **Lab4Web**
2. Kerjakan seluruh latihan secara berurutan
3. Screenshot setiap hasilnya
4. Buat file **README.md** dan isi dengan penjelasan langkah-langkah ini
5. Commit semua file ke repository
6. Kirim link repository ke **Ecampus Universitas Pelita Bangsa**

---

## ✅ Kesimpulan

Dalam praktikum ini, mahasiswa telah mempelajari:

* Struktur dasar layout web dengan HTML5 Semantic Elements.
* Konsep Box Element dan CSS Float.
* Cara membuat layout sederhana dengan navigasi, hero, sidebar, dan footer.
* Membuat halaman tambahan **About** dan **Contact** sesuai tugas.

---
