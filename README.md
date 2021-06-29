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

