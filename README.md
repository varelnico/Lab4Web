# Lab4Web - Praktikum 4: CSS Layout

## Nama : Varel Nico Ramadhan
## NIM : 312510156
## Kelas : I251B  
## Mata Kuliah : Pemrograman Web  

---

### Membuat Box Element
Menambahkan elemen `<section>` yang berisi tiga `<div>` dengan class berbeda (`div1`, `div2`, `div3`). Setiap `div` berperan sebagai satu "kotak" (box). Secara default, `div` adalah elemen *block* sehingga tampil menumpuk ke bawah.

<img width="1920" height="1080" alt="code 1" src="https://github.com/user-attachments/assets/8be5e084-1485-4868-bad8-6a32eb506dda" />
<img width="1920" height="1080" alt="hasil 1" src="https://github.com/user-attachments/assets/973c6c06-9747-49c0-9ea2-286ca8762e44" />
 

### CSS Float Property
Menambahkan blok `<style>` pada `<head>`. Properti `float: left` membuat setiap `div` "mengambang" ke kiri sehingga tersusun **berdampingan** secara horizontal, bukan menumpuk. `padding` memberi jarak antara isi dan tepi box, sedangkan `background` memberi warna berbeda agar setiap box mudah dibedakan.

<img width="1920" height="1080" alt="code 2" src="https://github.com/user-attachments/assets/70f8db40-bb65-41f3-b25e-23099c593d18" />
<img width="1920" height="1080" alt="hasil 2" src="https://github.com/user-attachments/assets/efc4846d-9dab-4cce-a2b9-5ab47fa2782f" />


### Mengatur Clearfix
Elemen yang berada setelah elemen float akan ikut "naik" dan menyesuaikan posisi float tersebut. Untuk mengatasinya, ditambahkan `div4` dengan properti `clear` agar elemen ini tampil di bawah elemen float sebelumnya, dan `float: none` agar tidak ikut mengambang. Praktikan juga diminta bereksperimen dengan nilai `clear` lain (`left`, `right`, `both`) untuk memahami pengaruhnya.

<img width="1920" height="1080" alt="code 2" src="https://github.com/user-attachments/assets/fead291c-157c-4b29-a63a-d16e48758f7e" />
<img width="1920" height="1080" alt="hasil 2" src="https://github.com/user-attachments/assets/89aadac9-0913-417a-a414-b338938b5125" />


### Membuat Layout Sederhana
Halaman dibagi ke dalam elemen semantik HTML5 sesuai fungsinya:
- `<header>`: bagian kepala/judul situs
- `<nav>`: menu navigasi
- `<section id="hero">`: panel utama/banner
- `<section id="wrapper">`: pembungkus area konten, berisi `<section id="main">` (konten utama) dan `<aside id="sidebar">` (sidebar)
- `<footer>`: bagian kaki halaman

Mengimpor font **Open Sans** dari Google Fonts, lalu menerapkan *reset CSS* (`margin` dan `padding` diatur ke 0) agar tampilan konsisten di semua browser. Selain itu diatur gaya dasar `body` (font, ukuran, warna teks) dan `#container` (lebar tetap, posisi di tengah, serta bayangan tipis).

<img width="1920" height="1080" alt="code 3" src="https://github.com/user-attachments/assets/ed6cb5a0-238e-4b30-8c28-2d96e838fcdb" />
<img width="1920" height="1080" alt="hasil 3" src="https://github.com/user-attachments/assets/89fc3014-b8a4-42e0-9850-11e6ea32b59c" />


### Membuat Navigasi
Menu diberi latar biru dan link dibuat `inline-block` agar tersusun mendatar dengan padding yang nyaman diklik. Link diberi teks putih tanpa garis bawah. Link yang aktif atau saat di-*hover* berubah warna latar sebagai penanda interaksi.

<img width="1920" height="1080" alt="code 4" src="https://github.com/user-attachments/assets/6060e79d-d5d5-4ac3-bd02-be47b3bacde7" />
<img width="1920" height="1080" alt="hasil 4" src="https://github.com/user-attachments/assets/a2acb4cd-c9f2-441f-a290-705b367c2a5d" />


### Membuat Hero Panel
Menambahkan konten HTML pada section `hero`: judul, paragraf, dan tombol *Learn more*. CSS memberi latar abu-abu, padding, margin, serta ukuran font dan jarak baris pada judul dan paragraf agar menonjol sebagai bagian pembuka halaman.

<img width="1920" height="1080" alt="code 5" src="https://github.com/user-attachments/assets/f7e9dbde-a4f9-46fb-8d43-c5bbaac342d0" />
<img width="1920" height="1080" alt="code 5_1" src="https://github.com/user-attachments/assets/0d260567-0419-468d-89db-2ac4bac81d82" />
<img width="1920" height="1080" alt="hasil 5" src="https://github.com/user-attachments/assets/88a308e7-296d-4b4f-9948-fb7dbc798d75" />


### Mengatur Layout Main dan Sidebar
Menggunakan **float** untuk membuat tampilan dua kolom. `#main` (lebar 640px) dan `#sidebar` (lebar 260px) sama-sama di-float ke kiri sehingga sejajar. Total lebar kedua kolom (beserta padding) menyesuaikan lebar container 980px.

<img width="1920" height="1080" alt="Screenshot (320)" src="https://github.com/user-attachments/assets/041ad758-7afd-4992-b99c-e7273d15aeeb" />
<img width="1920" height="1080" alt="code 6_1" src="https://github.com/user-attachments/assets/9a4af75f-6d54-41dd-a08c-9b80d2c4e1f1" />

Mengisi sidebar dengan dua widget (`widget-box`): satu berisi daftar link, satu berisi teks. CSS memberi border tipis, judul widget berlatar biru, daftar tanpa bullet, serta efek hover pada link agar lebih interaktif.  

<img width="1920" height="1080" alt="code 6_2" src="https://github.com/user-attachments/assets/24ded5ab-72ef-4a8e-a53f-2157e359e1c7" />
<img width="1920" height="1080" alt="hasil 6" src="https://github.com/user-attachments/assets/a6d45356-b8da-4a83-b300-d4c47f630759" />


### Mengatur Footer
Footer diberi `clear: both` agar berada di bawah kedua kolom yang di-float dan tidak naik ke samping. Selain itu diberi latar gelap, padding, dan teks berwarna terang.

<img width="1920" height="1080" alt="code 7" src="https://github.com/user-attachments/assets/f382418e-5a1e-473f-be1a-99fae7527ef9" />
<img width="1920" height="1080" alt="hasil 7" src="https://github.com/user-attachments/assets/4ce34f5d-1dac-4890-afd1-f8703ff02e9d" />


### Menambahkan Elemen pada Main Content
Menambahkan tiga kolom `.box` di dalam `.row`, masing-masing berisi gambar bulat, heading, deskripsi singkat, dan tombol *View detail*. CSS yang digunakan:
- Setiap box memakai lebar 33.33% dan di-float ke kiri, sehingga tersusun tiga kolom sejajar.
- `box-sizing: border-box` agar padding tidak menambah lebar total elemen.
- `border-radius: 50%` membuat gambar berbentuk lingkaran.
- Teknik clearfix dengan `:before` dan `:after` pada `.row` agar container tetap membungkus elemen yang di-float.

<img width="1920" height="1080" alt="code 8_1" src="https://github.com/user-attachments/assets/e7615072-9055-41fa-b5f4-ca4ddac3bd09" />
<img width="1920" height="1080" alt="code 8_2" src="https://github.com/user-attachments/assets/dac6b66d-7932-4925-8897-52e8fe22a009" />
<img width="1920" height="1080" alt="hasil 8" src="https://github.com/user-attachments/assets/bebe5217-ad5c-42fc-a7db-77357630bd49" />


### Menambahkan Content Artikel
Menambahkan dua `<article class="entry">` yang dipisahkan garis pembatas (`<hr class="divider">`). Masing-masing berisi heading, gambar, dan paragraf. Gambar pada artikel pertama di-float ke kiri dan pada artikel kedua ke kanan, sehingga teks mengalir di sisi gambar. CSS juga mengatur margin, jarak antar elemen, sudut gambar yang membulat, dan gaya garis pembatas.

<img width="1920" height="1080" alt="code 9_1" src="https://github.com/user-attachments/assets/9af9435c-53bc-4dae-8081-3adb74a6399f" />
<img width="1920" height="1080" alt="code 9_2" src="https://github.com/user-attachments/assets/eb282dff-dd6c-46d5-aaa1-fc8792027351" />
<img width="1920" height="1080" alt="hasil 9" src="https://github.com/user-attachments/assets/c78e4f7c-11c6-4516-92af-f1d2978be15e" />
  

### Menambahkan Layout Untuk Menu About

<img width="975" height="855" alt="kode 10" src="https://github.com/user-attachments/assets/6851306f-95ee-411e-bdfa-3ac0a37bed64" />
<img width="957" height="805" alt="kode 10_2" src="https://github.com/user-attachments/assets/ea28f1f9-14a6-4d09-9f75-9ff4f0736c63" />
<img width="909" height="473" alt="kode 10_3" src="https://github.com/user-attachments/assets/9209a783-7312-43c6-8446-4d6b010f311b" />
<img width="982" height="949" alt="hasil 10" src="https://github.com/user-attachments/assets/aa9ecd65-8936-4e50-89a6-ff57e80d3a71" />
<img width="989" height="922" alt="hasil 10_2" src="https://github.com/user-attachments/assets/66daf38b-6e0e-4778-bf84-3ac2d485fce1" />


### Menambahkan Layout Untuk Menu Contact

<img width="1013" height="709" alt="kode 11" src="https://github.com/user-attachments/assets/0a09b8ac-7d16-4787-a0f5-de79e2cb7754" />
<img width="833" height="551" alt="kode 11_2" src="https://github.com/user-attachments/assets/b89e6702-87e0-4ea7-89dd-c3788c0abb9b" />
<img width="476" height="761" alt="kode 11_3" src="https://github.com/user-attachments/assets/1c75352a-95d2-4ce7-8282-d514c461632e" />
<img width="688" height="941" alt="hasil 11" src="https://github.com/user-attachments/assets/b28ca600-a34d-43df-b503-cb3527d0d9fa" />
