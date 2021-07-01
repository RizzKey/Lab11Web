# Praktikum 11 - Codeigniter - Pemrograman Web

```
Fitrah Rizki Ardiansyah
311910465
TI.19.A.2
```
# yang harus diPersiapkan
Beberapa ekstensi PHP perlu diaktifkan untuk kebutuhan pengembangan Codeigniter 4

# langkah 1 
Untuk mengaktifkan ekstentsi tersebut melalui ```XAMPP Control Panel```, pada bagian ```Apache``` klik Config -> ```PHP.ini```![SS 1](https://user-images.githubusercontent.com/56240954/122005618-10040780-cde0-11eb-9deb-1f7a92a6111e.png)
![SS 2](https://user-images.githubusercontent.com/56240954/122005888-61ac9200-cde0-11eb-8567-dd8328f3340d.png)

Kemudian buat folder baru dengan nama ```lab11_php_ci``` pada doc root webserver ```(htdocs)```![SS 3](https://user-images.githubusercontent.com/56240954/122006610-3b3b2680-cde1-11eb-9cfb-fba8c668d7c2.png)

# Langkah 2
Instalasi CodeIgniter 4
```
Codeigniter dapat didownload dari website https://codeigniter.com/download
Extrak file zip Codeigniter ke direktori htdocs/lab11_php_ci.
Ubah nama directory framework-4.x.xx menjadi ci4.
Buka browser dengan alamat http://localhost/lab11_php_ci/ci4/public/ Untuk melakukan instalasi Codeigniter 4 dapat dilakukan dengan dua cara, yaitu cara manual dan menggunakan composer. Pada praktikum ini kita menggunakan cara manual seperti berikut.
```
![SS 5](https://user-images.githubusercontent.com/56240954/123743581-a142a600-d8d7-11eb-96a1-4af39f9ac877.png)

# Langkah 3
# Menjalankan CLI (Command Line Interface)

Codeigniter 4 menyediakan CLI untuk mempermudah proses development. Untuk mengakses CLI buka terminal/command prompt, lalu arahkan lokasi direktori sesuai dengan direktori kerja project dibuat (C:\xampp\htdocs\Lab11_php_ci\ci4). Kemudian setelah itu jalankan perintah untuk 
memanggil CLI Codeigniter seperti berikut 
  ![SS 3](https://user-images.githubusercontent.com/56240954/123743698-ce8f5400-d8d7-11eb-9653-cc2d43964a29.png)
    
# Langkah 4
# Mengaktifkan Mode Debugging

Codeigniter 4 menyediakan fitur debugging untuk memudahkan developer untuk mengetahui pesan error apabila terjadi kesalahan dalam membuat kode program. Secara default fitur ini belum aktif. Ketika terjadi error pada aplikasi akan ditampilkan pesan kesalahan seperti berikut. 

![SS LANGKAH 4](https://user-images.githubusercontent.com/56240954/123744057-67be6a80-d8d8-11eb-9b20-78f9edf3e35d.png)
Semua jenis error akan ditampilkan sama. Untuk memudahkan mengetahui jenis errornya, maka perlu mengaktifkan mode debugging dengan mengubah nilai konfigurasi pada environment variable CI_ENVIRONMENT menjadi development. Kemudian mengubah nama file env menjadi .env lalu setelah itu buka file tersebut dan ubah nilai variable CI_ENVORNMENT menjadi development. Setelah mengubah nilai konfigurasi pada environment variable CI_ENVIRONMENT menjadi development. maka hapus tanda tagar (#) pada awal baris CI_ENVIRONMENT. Dan yang terakhir, ubah kode pada file app/Controller/Home.php kemudian hilangkan titik koma (;) pada akhir kode seperti berikut.
![SSSS](https://user-images.githubusercontent.com/56240954/123744677-4ad66700-d8d9-11eb-95fb-973c48a897b1.png)
Maka hasilnya akan terjadi error seperti berikut.
![SS LANGKAH 4 (Tambahan 2)](https://user-images.githubusercontent.com/56240954/123745156-0dbea480-d8da-11eb-996b-182d8bcfbd6d.png)

# Langkah 5
# Membuat Route Baru.

Menambahkan kode di dalam Routes.php seperti berikut. 
![SS LANGKAH 5](https://user-images.githubusercontent.com/56240954/123745665-cdabf180-d8da-11eb-9c48-2006266a8e2f.png)

Untuk mengetahui route yang ditambahkan sudah benar, buka CLI dan jalankan perintah berikut.
![SS LANGKAH 5 (TAMBAHAN)](https://user-images.githubusercontent.com/56240954/123746240-925df280-d8db-11eb-9fdd-64966fee644b.png)

Selanjutnya coba akses route yang telah dibuat dengan mengakses alamat url http://localhost:8080/about seperti berikut. Maka hasilnya akan terjadi error, yang artinya file/page tersebut tidak ada. Untuk dapat mengakses halaman tersebut, harus dibuat terlebih dahulu Contoller yang sesuai dengan routing yang dibuat yaitu Contoller Page.
![SS LANGKAH 5 (Tambahan 2)](https://user-images.githubusercontent.com/56240954/123746519-f385c600-d8db-11eb-95ec-23a38c7591b6.png)

# Langkah 6
# Membuat Controller

Selanjutnya adalah membuat Controller Page. Buat file baru dengan nama page.php pada direktori Controller kemudian isi kodenya seperti berikut
![SS LANGKAH 6](https://user-images.githubusercontent.com/56240954/123747015-8f173680-d8dc-11eb-9f70-d22f4c5955ea.png)

# Langkah 7
# Auto Routing

Secara default fitur autoroute pada Codeiginiter sudah aktif. Untuk mengubah status autoroute dapat mengubah nilai variabelnya. Untuk menonaktifkan ubah nilai true menjadi false. Kemudian tambahkan method baru pada Controller Page seperti berikut. Method ini belum ada pada routing, sehingga cara mengaksesnya dengan menggunakan alamat: http://localhost:8080/page/tos
![SS LANGKAH 7](https://user-images.githubusercontent.com/56240954/123747277-eb7a5600-d8dc-11eb-8154-e606c8b674b9.png)

# Langkah 8
# Membuat View

Selanjutnya adalah membuat view untuk tampilan web agar lebih menarik. Buat file baru dengan nama about.php pada direktori view (app/view/about.php) kemudian isi kodenya seperti berikut. Kemudian ubah method about pada class Controller Page menjadi seperti berikut.
![SS LANGKAH 8](https://user-images.githubusercontent.com/56240954/123753883-8296dc00-d8e4-11eb-80e6-39ce84d9b338.png)
Maka hasilnya akan seperti berikut.
![SS LANGKAH 8 (TAMBAHAN)](https://user-images.githubusercontent.com/56240954/123754279-ea4d2700-d8e4-11eb-93f2-d9f09be90a2f.png)

# Langkah 9
# Membuat Layout Web dengan CSS
Pada dasarnya layout web dengan css dapat diimplementasikan dengan mudah pada Codeigniter. Yang perlu diketahui adalah pada Codeigniter 4 file yang menyimpan asset css dan javascript terletak pada direktori public. Buat file css pada direktori public dengan nama style.css seperti berikut.
![SS LANGKAH 9](https://user-images.githubusercontent.com/56240954/123755096-c3432500-d8e5-11eb-8b34-fceb20f4b5fd.png)
Kemudian buat folder template pada direktori view ke mudian buat file header.php dan footer.php seperti berikut. SS LANGKAH 9 (TAMBAHAN)
![SS LANGKAH 9 (TAMBAHAN)](https://user-images.githubusercontent.com/56240954/123755809-7e6bbe00-d8e6-11eb-8be6-c73b413c304e.png)
Maka hasilnya seperti berikut.
![SS LANGKAH 9 (TAMBAHAN 2)](https://user-images.githubusercontent.com/56240954/123756428-1a95c500-d8e7-11eb-9033-a154f297b1ac.png)

# Pertanyaan dan Tugas
Lengkapi kode program untuk menu lainnya yang ada pada Controller Page, sehingga semua link pada navigasi header dapat menampilkan tampilan dengan layout yang sama.

# Hasilnya
![SS 2](https://user-images.githubusercontent.com/56240954/123756665-5af54300-d8e7-11eb-8f2e-7a3ab4b36b03.png)
![SS JAWABAN 2](https://user-images.githubusercontent.com/56240954/123757228-f4245980-d8e7-11eb-8417-ef35ec2d1685.png)

# Praktikum 12: Framework Lanjutan (CRUD) - Pemrograman Web
## Langkah-langkah Praktikum
## Persiapan
Untuk memulai membuat aplikasi CRUD sederhana, yang perlu disiapkan adalah database server menggunakan MySQL. Pastikan MySQL Server sudah dapat dijalankan melalui XAMPP seperti berikut. SS XAMPP
![SS XAMPP](https://user-images.githubusercontent.com/56240954/123760069-b4ab3c80-d8ea-11eb-8804-a6a4af88e0c1.png)

# Langkah 1

 Membuat database kemudian membuat Tabel dan masukkan kode pada database query seperti berikut.
![SS LANGKAH 1](https://user-images.githubusercontent.com/56240954/123760905-7bbf9780-d8eb-11eb-8744-dc5098525c7e.png)

# Langkah 2
Konfigurasi koneksi database

Selanjutnya membuat konfigurasi untuk menghubungkan dengan database server. Kemudian melakukan konfigurasi dengan cara mengubah beberapa kode pada file htdocs\lab11_php_ci\ci4\.env. Lalu cari pada line DATABASE dan hilangkan tanda pagar (#) didepan seperti berikut ini. 
![SS LANGKAH 2](https://user-images.githubusercontent.com/56240954/123761275-da851100-d8eb-11eb-81c3-c3b4448a86a5.png)

# Langkah 3
Membuat Model

Selanjutnya adalah membuat Model untuk memproses data Artikel. Buat file baru pada direktori app/Models dengan nama ArtikelModel.php lalu masukkan kode seperti berikut
![SS LANGKAH 3](https://user-images.githubusercontent.com/56240954/123761837-65fea200-d8ec-11eb-9a22-d87fac112387.png)

# Langkah 4
Membuat Controller

Buat Controller baru dengan nama Artikel.php pada direktori app/Controllers lalu masukkan kode seperti berikut. SS LANGKAH 4
![SS LANGKAH 4](https://user-images.githubusercontent.com/56240954/123762251-d3123780-d8ec-11eb-97ba-3002dfe78bfa.png)

# Langkah 5
Membuat View

Buat folder baru dengan nama artikel pada direktori app/views, kemudian buat file baru dengan nama index.php seperti berikut.
![SS LANGKAH 5](https://user-images.githubusercontent.com/56240954/123762680-3c924600-d8ed-11eb-93fd-5346b4117f2d.png)
Selanjutnya buka browser kembali, dengan mengakses url http://localhost:8080/artikel maka hasilnya akan seperti berikut. 
![SS LANGKAH 5 (TAMBAHAN)](https://user-images.githubusercontent.com/56240954/123763223-c3dfb980-d8ed-11eb-8127-2d158bbf8bcd.png)
Terlihat belum ada data yang diampilkan. Kemudian coba tambahkan beberapa data pada database query agar dapat ditampilkan datanya seperti berikut.![SS LANGKAH 5 (TAMBAHAN 2)](https://user-images.githubusercontent.com/56240954/123764323-e0302600-d8ee-11eb-9bb4-47819fbeb2cf.png)
Lalu refresh kembali browser, sehingga akan ditampilkan hasilnya seperti berikut
![SS LANGKAH 5 (TAMBAHAN 3)](https://user-images.githubusercontent.com/56240954/123764872-65b3d600-d8ef-11eb-9b9e-5e2281005897.png)

# Langkah 6
Membuat Tampilan Detail Artikel

Tampilan pada saat judul berita di klik maka akan diarahkan ke halaman yang berbeda. Tambahkan fungsi baru pada Controller Artikel dengan nama view() seperti berikut.
![SS LANGKAH 6](https://user-images.githubusercontent.com/56240954/123765634-1e7a1500-d8f0-11eb-97b2-f1ffb8fc334a.png)

# Langkah 7
Membuat View Detail

Buat view baru untuk halaman detail dengan nama app/views/artikel/detail.php seperti berikut. SS LANGKAH 7
![SS LANGKAH 7](https://user-images.githubusercontent.com/56240954/123766074-8c264100-d8f0-11eb-8dd7-c058e90753ff.png)

# Langkah 8
Membuat Routing untuk artikel detail

Buka kembali file app/config/Routes.php, kemudian tambahkan routing untuk artikel detail maka hasilnya akan seperti berikut. SS LANGKAH 8
![SS LANGKAH 8](https://user-images.githubusercontent.com/56240954/123766881-4322bc80-d8f1-11eb-8fb1-b55e38bde35c.png)

# Langkah 9
Membuat Menu Admin

Menu admin adalah untuk proses CRUD data artikel. Buat method baru pada Controller Artikel dengan nama admin_index() seperti berikut. 
![SS LANGKAH 9](https://user-images.githubusercontent.com/56240954/123767431-a7458080-d8f1-11eb-906c-8c46da57dc93.png)
Selanjutnya buat view untuk tampilan admin dengan nama admin_index.php seperti berikut. 
![SS LANGKAH 9 (TAMBAHAN 2)](https://user-images.githubusercontent.com/56240954/123768017-276be600-d8f2-11eb-9bab-0bc1f390a7d5.png)
Setelah itu tambahkan routing untuk menu admin seperti berikut. 
![SS LANGKAH 9 (TAMBAHAN 3)](https://user-images.githubusercontent.com/56240954/123768769-d4466300-d8f2-11eb-8ecb-4164ea970186.png)
Setelah itu buat template header dan footer baru untuk Halaman Admin. Kemudian buat file baru dengan nama admin_header.php pada direktori app/view/template seperti berikut. 
![TAMBAHAN 1](https://user-images.githubusercontent.com/56240954/123769861-ed034880-d8f3-11eb-95d4-6890d081845c.png)
Lalu buat file baru lagi dengan nama admin_footer.php pada direktori app/view/template seperti berikut. 
![TAMBAHAN 2](https://user-images.githubusercontent.com/56240954/123770106-30f64d80-d8f4-11eb-964f-02685d3615c5.png)
Dan yang terakhir buat file baru lagi dengan nama admin.css pada direktori ci4/public untuk memperindah tampilan Halaman Admin seperti berikut
![TAMBAHAN 3](https://user-images.githubusercontent.com/56240954/123770422-7adf3380-d8f4-11eb-9c0b-24e59cd19747.png)
![TAMBAHAN 4](https://user-images.githubusercontent.com/56240954/123770692-ad892c00-d8f4-11eb-920a-f3640856a5ba.png)

Kemudian akses menu admin dengan url http://localhost:8080/admin/artikel seperti berikut.
![Langkah 9](https://user-images.githubusercontent.com/56240954/123911873-855a0580-d9a6-11eb-858c-ad569c584083.png)

# Langkah 10
Menambah Data Artikel

Tambahkan fungsi/method baru pada Controller Artikel dengan nama add() seperti berikut. 
![Langkah 10](https://user-images.githubusercontent.com/56240954/123914773-f5b65600-d9a9-11eb-82ba-dbd7824ef956.png)
Kemudian buat view untuk form tambah dengan nama form_add.php seperti berikut.
![Langkah 10 A](https://user-images.githubusercontent.com/56240954/123915177-6b222680-d9aa-11eb-8e3e-bba60b20c909.png)
Setelah itu, lalu klik Tambah Artikel pada menu Halaman Admin Maka hasilnya akan seperti berikut.
![Langkah 10 b](https://user-images.githubusercontent.com/56240954/123915248-7f662380-d9aa-11eb-8639-d1ac8ddfb791.png)

# Langkah 11
Mengubah Data

Tambahkan fungsi/method baru pada Controller Artikel dengan nama edit() seperti berikut. 
![Langkah 11](https://user-images.githubusercontent.com/56240954/123915287-8a20b880-d9aa-11eb-8c56-ef7c59601583.png)
Kemudian buat view untuk form tambah dengan nama form_edit.php
![Langkah 11 A](https://user-images.githubusercontent.com/56240954/123915397-a91f4a80-d9aa-11eb-8760-8d119425993c.png)
Setelah itu, lalu klik Ubah pada salah satu judul artikel, maka hasilnya akan seperti berikut. 
![Langkah 11 B](https://user-images.githubusercontent.com/56240954/123915535-cfdd8100-d9aa-11eb-870b-28dc5246ec80.png)

# Langkah 12
Menghapus Data

Tambahkan fungsi/method baru pada Controller Artikel dengan nama delete() seperti berikut.
![Langkah12](https://user-images.githubusercontent.com/56240954/123915809-1af79400-d9ab-11eb-9715-d34258f9d26e.png)


# Praktikum 13: Framework Lanjutan (Modul Login)
## Langkah-langkah Praktikum
## Persiapan

Untuk memulai membuat modul Login, yang perlu dipersiapkan adalah database server menggunakan MySQL. Pastikan MySQL Server sudah dapat dijalankan melalui XAMPP seperti berikut. 
![ss xamp](https://user-images.githubusercontent.com/56240954/123917663-3cf21600-d9ad-11eb-98a5-38852deb7a66.png)

# Langkah 1
## Membuat Tabel User

Membuat tabel user pada database ```lab_ci4``` seperti berikut. 
![SS 1](https://user-images.githubusercontent.com/56240954/123917729-51cea980-d9ad-11eb-9491-eb0a04df1f80.png)

# Langkah 2
## Membuat Model User

Selanjutnya adalah membuat Model untuk memproses data Login. Buat file baru pada direktori app/Models dengan nama UserModel.php dan masukkan kode seperti berikut. 
![Langkah2](https://user-images.githubusercontent.com/56240954/123917787-60b55c00-d9ad-11eb-812e-4501551913e5.png)

# Langkah 3
## Membuat Controller User

Buat Controller baru dengan nama User.php pada direktori app/Controllers. Kemudian tambahkan method index() untuk menampilkan daftar user, dan method login() untuk proses login dan masukkan kode seperti berikut. SS LANGKAH 3
![Langkah 3](https://user-images.githubusercontent.com/56240954/124060118-8ba7ba80-da56-11eb-94fe-e2485d55ef87.png)
![Langkah 3 A](https://user-images.githubusercontent.com/56240954/124060318-feb13100-da56-11eb-9029-9a555bc1a2af.png)

# Langkah 4
## Membuat View Login

Buat folder baru dengan nama user pada direktori app/views, kemudian buat file baru dengan nama login.php dan masukkan kode seperti berikut. 
![Langkah 4](https://user-images.githubusercontent.com/56240954/124060379-21434a00-da57-11eb-98e4-39b6ed5ca37a.png)

# Langkah 5
Membuat Database Seeder

Database seeder digunakan untuk membuat data dummy. Untuk keperluan ujicoba modul login, kita perlu memasukkan data user dan password kedalam database. Untuk itu buat database seeder untuk tabel user. Buka CLI, kemudian ketik perintah berikut:
![Langkah 5](https://user-images.githubusercontent.com/56240954/124069479-75095f80-da66-11eb-9696-a731ba4e6719.png)
Selanjutnya, buka file UserSeeder.php yang berada di lokasi direktori /app/Database/Seeds/UserSeeder.php kemudian isi dengan kode berikut: 
![langkah 5 A](https://user-images.githubusercontent.com/56240954/124069538-8b172000-da66-11eb-9ffc-5c46a2821120.png)
Selanjutnya buka kembali CLI dan ketik perintah berikut: 
![Langkah 5 B](https://user-images.githubusercontent.com/56240954/124069625-ab46df00-da66-11eb-9dfe-a64696d8644f.png)
Namun sebelum mengakses urlnya, pastikan untuk menjalankan perintah php spark serve terlebih dahulu untuk menjalankan program ci4 di port 8080 dengan cara membuka CLI kemudian ketik perintah berikut: SS LANGKAH 5
![Langkah 5 C](https://user-images.githubusercontent.com/56240954/124069715-d5000600-da66-11eb-8af7-e23e84d7efac.png)

# Langkah 6
## Menambahkan Auth Filter

Selanjutnya membuat filter untuk halaman admin. Buat file baru dengan nama Auth.php pada direktori app/Filters dan masukkan kode seperti berikut. 
![Langkah 6](https://user-images.githubusercontent.com/56240954/124069787-f52fc500-da66-11eb-9127-f05e4638ed1c.png)
Selanjutnya buka file app/Config/Routes.php dan sesuaikan kodenya seperti berikut.
![Langkah 6 A](https://user-images.githubusercontent.com/56240954/124069899-2f996200-da67-11eb-86e5-13901a914416.png)
Selanjutnya buka file app/Config/Routes.php dan sesuaikan kodenya seperti berikut
![Langkah 6 B](https://user-images.githubusercontent.com/56240954/124069969-4d66c700-da67-11eb-833c-b172968f1e7e.png)

# Langkah 7
## Fungsi Logout

Tambahkan method logout pada Controller User dan masukkan kode seperti berikut: SS LANGKAH 7
![Langkah 7](https://user-images.githubusercontent.com/56240954/124071063-0548a400-da69-11eb-8015-812e68411bfe.png)

# Langkah 8
## Tombol Logout

Menambahkan tombol Logout pada menu header admin dengan cara ke direktori app\view\template lalu buka file admin_header.php dan masukkan kode seperti berikut. 
![Langkah 8](https://user-images.githubusercontent.com/56240954/124071255-450f8b80-da69-11eb-8098-e151148c1c80.png)
Selanjutnya, tambahkan route logout dengan cara ke direktori app\Config\Routes.php dan masukkan kode seperti berikut.
![Langkah 8 A](https://user-images.githubusercontent.com/56240954/124071354-64a6b400-da69-11eb-9984-d62394efbf7a.png)
Berikut adalah halaman utama (menu admin) yang sudah ditambahkan tombol Logout untuk keluar dari menu ini dan kembali ke menu Login. 
![Langkah 8 B](https://user-images.githubusercontent.com/56240954/124071475-928bf880-da69-11eb-8f2a-9a2d3faa3776.png)





