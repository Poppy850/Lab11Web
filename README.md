# Lab11Web
Nama : Poppy Harandtika
NIM : 311910687
Kelas : TI.19.C1

![SS XAMPP](https://user-images.githubusercontent.com/85287196/122388183-75611100-cf24-11eb-8f4a-193c2efe6b11.png)

![htdoct](https://user-images.githubusercontent.com/85287196/122388220-8447c380-cf24-11eb-8977-10f9b6aff8fd.png)

![welcome codeineinter](https://user-images.githubusercontent.com/85287196/122596537-dd941d80-d01e-11eb-8ed3-ca0ee7f74c5e.png)

Menjalankan CLI (Command Line Interface)
Codeigniter 4 menyediakan CLI untuk mempermudah proses development. Untuk mengakses CLI buka terminal/command prompt.
![env](https://user-images.githubusercontent.com/85287196/122596673-146a3380-d01f-11eb-811c-9ea74c45b2ca.png)

Perintah yang dapat dijalankan untuk memanggil CLI Codeigniter adalah:
![spark route](https://user-images.githubusercontent.com/85287196/122596617-fef50980-d01e-11eb-87c9-fe9349813858.png)


Ubah nama file env menjadi .env kemudian buka file tersebut dan ubah nilai variable
CI_ENVIRINMENT menjadi development.
![parse eror](https://user-images.githubusercontent.com/85287196/122596817-4a0f1c80-d01f-11eb-9a1f-61b6b06133b5.png)

Membuat Controller
Selanjutnya adalah membuat Controller Page. Buat file baru dengan nama page.php pada direktori Controller kemudian isi kodenya seperti berikut.
![ini halaman about](https://user-images.githubusercontent.com/85287196/122596945-7e82d880-d01f-11eb-9004-0d48b1b25d61.png)

Ubah method about pada class Controller Page menjadi seperti berikut:
Kemudian lakukan refresh pada halaman tersebut
![halaman about](https://user-images.githubusercontent.com/85287196/122597075-b722b200-d01f-11eb-88e9-477cc20decfb.png)

Buat file css pada direktori public dengan nama style.css (copy file dari praktikum lab4_layout).
![css](https://user-images.githubusercontent.com/85287196/122661563-84bca600-d140-11eb-912e-d29ff847ddf0.png)

Kemudian buat folder template pada direktori view, lalu buat file header.php dan footer.php.
![image](https://user-images.githubusercontent.com/85287196/122661575-a584fb80-d140-11eb-8e97-72263e6df71c.png)
![image](https://user-images.githubusercontent.com/85287196/122661583-bb92bc00-d140-11eb-9dc2-594696d79f25.png)

Pertanyaan Tugas
Lengkapi kode program untuk menu lainnya yang ada pada Controller Page, 
sehingga semua link pada navigasi header dapat menampilkan tampilan dengan layout yang sama.
![image](https://user-images.githubusercontent.com/85287196/122661595-d402d680-d140-11eb-8596-2351a8105854.png)

![selamat datang halaman web](https://user-images.githubusercontent.com/85287196/122597347-154f9500-d020-11eb-98a6-76d7eb7b499b.png)


Lab12Web
Nama : Poppy Harandtika 
NIM : 311910687
Kelas : TI.19.C1

Praktikum 12 - Pemrograman Web (Framework Lanjutan - CRUD)
Pastikan MySQL server sudah berjalan dan buat sebuah database sebagai berikut: 
![localhost 12](https://user-images.githubusercontent.com/85287196/122661817-3957c700-d143-11eb-975b-9b8d6c63beeb.JPG)

Konfigurasi Database
Membuat konfigurasi hubungan ke database server dengan menggunakan file .env.
![image](https://user-images.githubusercontent.com/85287196/122662086-365dd600-d145-11eb-887d-3d8f19528b78.png)

Membuat Model
Buat file baru pada direktori /app/Models dengan nama ArtikelModel.php
![image](https://user-images.githubusercontent.com/85287196/122662099-48d80f80-d145-11eb-8075-38d4095b0755.png)

Membuat COntrolleR
Buat Controller baru dengan nama Artikel.php pada direktori /app/Controllers.
![image](https://user-images.githubusercontent.com/85287196/122662117-58efef00-d145-11eb-8820-56a164dfd9fc.png)

Membuat View
Buat direktori baru dengan nama artikel pada direktori /app/Views, kemudian buat file baru dengan nama index.php.
![image](https://user-images.githubusercontent.com/85287196/122662124-660cde00-d145-11eb-8f70-d24a99b4d297.png)

Lalu buka alamat http://localhost:8080/artikel untuk melihat hasilnya. Tidak ada data yang ditampilkan karena database masih kosong.
![image](https://user-images.githubusercontent.com/85287196/122662131-745afa00-d145-11eb-97a0-4c250b498d79.png)

Tambahkan data pada database untuk ditampilkan datanya.
![image](https://user-images.githubusercontent.com/85287196/122662142-8341ac80-d145-11eb-9825-bd9d06df51f6.png)

ketikaa di refresh akan muncul tampilan seperti ini. 
![image](https://user-images.githubusercontent.com/85287196/122662146-8fc60500-d145-11eb-83d6-e96476b61fca.png)

Membuat Tampilan Detail Artikel
Tampilan pada saat judul berita di klik maka akan diarahkan ke halaman yang berbeda. 
Tambahkan sebuah fungsi baru pada Controller Artikel (/app/Controllers/Artikel.php) dengan nama view().
![image](https://user-images.githubusercontent.com/85287196/122662150-994f6d00-d145-11eb-9b02-f331fd228d07.png)

Membuat View Detail
Buat file baru dalam folder artikel (/app/Views/artikel/) dengan nama detail.php untuk menampilkan halaman detail.
![image](https://user-images.githubusercontent.com/85287196/122662163-b6843b80-d145-11eb-961d-db51e0f21bfa.png)

Membuat Route
Buka file Routes.php dalam folder (/app/Config/) dan 
tambahkan routing untuk ke halaman detail artikel.
$routes->get('/artikel/(:any)', 'Artikel::view/$1');
![image](https://user-images.githubusercontent.com/85287196/122662171-c6038480-d145-11eb-8b60-9fcefd9294a1.png)

Maka akan tampil halaman dari artikel yang diklik. 
![image](https://user-images.githubusercontent.com/85287196/122662184-d4ea3700-d145-11eb-9a46-99c23b15555c.png)

Membuat Menu Admin
Menu admin adalah untuk proses CRUD data artikel. 
Buat method atau fungsi baru pada Controller Artikel dengan nama admin_index().
![image](https://user-images.githubusercontent.com/85287196/122662215-0ebb3d80-d146-11eb-808f-f9add2433d71.png)

Kemudian buat file admin_index.php dalam folder (/app/Views/artikel/) untuk tampilan halaman admin. 
![image](https://user-images.githubusercontent.com/85287196/122662234-2a264880-d146-11eb-9e02-8020e258cbe3.png)

![image](https://user-images.githubusercontent.com/85287196/122662247-3b6f5500-d146-11eb-8702-3696bddf01fb.png)

Menu admin dapat diakses dengan alamat http://localhost:8080/admin/artikel
![image](https://user-images.githubusercontent.com/85287196/122662268-72de0180-d146-11eb-8045-ccae4fc7b75d.png)

Menambah Data Artikel
Tambahkan fungsi/method baru pada Controller Artikel dengan nama add(). 
![image](https://user-images.githubusercontent.com/85287196/122662278-82f5e100-d146-11eb-9437-54982d7b661f.png)

Kemudian buat view untuk form tambah dengan nama form_add.php dalam folder (/app/Views/artikel/).
![image](https://user-images.githubusercontent.com/85287196/122662283-9143fd00-d146-11eb-820c-40fe8fe992fc.png)

Maka Tampilan nya Seperti ini
![image](https://user-images.githubusercontent.com/85287196/122662293-a9b41780-d146-11eb-85c4-813226b5cb2f.png)

Mengubah Data
Tambahkan fungsi/method baru pada Controller Artikel dengan nama edit().
![image](https://user-images.githubusercontent.com/85287196/122662300-ba648d80-d146-11eb-82a7-09c7aa72673f.png)

Kemudian buat view untuk form tambah dengan nama form_edit.php dalam folder (/app/Views/artikel/).
![image](https://user-images.githubusercontent.com/85287196/122662305-cb150380-d146-11eb-9177-63e97d362e4f.png)

Tampilan Ketika Mengubah Data
![image](https://user-images.githubusercontent.com/85287196/122662318-e5e77800-d146-11eb-8efd-f43384a74261.png)

Menghapus Data
Tambahkan fungsi/method baru pada Controller Artikel dengan nama delete().
![image](https://user-images.githubusercontent.com/85287196/122662327-f4359400-d146-11eb-8b74-5ab12a62be9b.png)

Pertanyaan dan Tugas
Selesaikan programnya sesuai Langkah-langkah yang ada. Anda boleh melakukan improvisasi.
Jawab : Saya Telah Menyelesaikan Program diatas dengan hingga semua berjalan dengan baik




























