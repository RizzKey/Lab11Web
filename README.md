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




