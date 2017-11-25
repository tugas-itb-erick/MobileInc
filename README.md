# Mobile, Inc.

![](logo/mobile-inc.jpg)

## Team
- Reinhard Benjamin Linardi (13515011)
- Erick Wijaya (13515057)
- Roland Hartanto (13515107)

## Deskripsi umum sistem

Sistem yang kami buat adalah sistem simulasi *resource management*. Sistem ini dibangun di atas 3 subsistem, yaitu subsistem Android, subsistem Unity, dan subsistem Arduino.

- Subsistem Unity merupakan subsistem utama berupa gamifikasi dari simulasi *resource management*. Pemain berperan sebagai manager sebuah perusahaan e-commerce bernama Mobile, Inc. Pemain harus mencapai target yang sudah diberikan dalam waktu tertentu dengan mengelola semua *resource* yang ada pada perusahaan.

- Subsistem Android merupakan simulasi dari aplikasi Mobile, Inc. Aplikasi ini digunakan oleh pengguna Mobile, Inc untuk memesan barang. Pengguna akan diberikan notifikasi jika data pesanan sudah diterima pada subsistem Unity. Pengguna juga dapat memanfaatkan kode promosi untuk mendapatkan diskon 10% jika pemain memutuskan untuk mengirimkan promosi pada subsistem Unity.

- Subsistem Arduino berperan sebagai sensor cuaca. Cuaca dikategorikan menjadi 2 bagian, yaitu cerah dan tidak cerah. Untuk mendeteksi cuaca, digunakan sensor kelembapan dan sensor suhu. Jika cuaca cerah, maka 7 segment akan menampilkan angka 1 dan lampu LED hijau akan menyala, sedangkan jika cuaca tidak cerah, maka 7 segment akan menampilkan angka 0 dan lampu LED merah akan menyala terang-redup (menggunakan PWM). Subsistem selanjutnya akan mengirim data ke subsistem Unity dengan *serial connection*.

## Panduan instalasi sistem

### Instalasi subsistem Android

1. Buka link berikut :
https://drive.google.com/a/std.stei.itb.ac.id/file/d/0B4a9OEwiZUdLQU1sZXpidW5GMFU/view?usp=sharing
2. Login dengan akun Webmail STEI
3. Download aplikasi Mobile, Inc (file .apk) pada link tersebut
4. Install pada device Android yang Anda inginkan

### Instalasi subsistem Unity

1. Buka link berikut :
https://drive.google.com/open?id=0B7EJUV7pyE6oMTFGeFFFY1pjbXc
2. Download archive (file .zip) pada link tersebut
3. Extract file archive pada folder yang Anda inginkan
4. Run file .exe untuk menjalankan aplikasi

### Instalasi subsistem Arduino

1. Download dan install Arduino IDE
2. Buka link berikut :
https://drive.google.com/open?id=1R2LVf0eJqQqwxEMbJ_Q9IvqCWonDNfAY
3. Download archive (file  .zip) pada link tersebut
4. Extract file archive pada folder yang Anda inginkan
5. Buka Arduino IDE, buka file *main.ino*
6. Pada menu bar, pilih Sketch > Include Library > Add ZIP Library. Pilih semua library yang ada pada file archive.
7. Pilih semua library dari list.
8. Sambungkan Arduino ke komputer.
9. Tekan tombol Upload. Program akan otomatis dikompilasi dan dijalankan oleh Arduino.


## Panduan penggunaan sistem

1. Jalankan file .exe pada subsistem Unity untuk memulai permainan.
2. Pilih Start, dan masukkan nama pemain.
3. Pada bar di atas akan muncul berbagai indikator.
	- **Target**, jumlah uang yang harus dikumpulkan untuk memenangkan permainan. Batas waktu tertulis di sebelahnya.
	- **Money**, uang yang dimiliki oleh pemain sekarang.
	- **Day**, waktu pada permainan. (hari ke berapa dan jam berapa sekarang)
	- **Happiness**, tingkat *happiness* pegawai.
	- **Trust**, tingkat kepercayaan konsumen.
	
	Semua parameter memberikan informasi tentang permainan saat ini. Jika **money**, **day**, atau **trust** bernilai terlalu negatif, pemain akan kalah.
	
	Bar tersebut juga memiliki info tentang stok barang dari masing-masing jenis *handphone* dan pesanan selanjutnya yang harus dipenuhi secepat mungkin.
4. Game terdiri atas 2 scene, yaitu kantor dan gudang. Pada scene kantor pemain dapat merekrut pegawai dan membeli barang-barang lain untuk meningkatkan produktivitas dan tingkat *happiness* pegawai. Pada scene gudang, pemain dapat melihat stok barang, mengirimkan pesanan, dan membeli barang jika stok habis.
5. Game dapat di-*pause* menggunakan tombol di kanan atas. Saat game sedang di-*pause*, waktu akan berhenti berjalan. Game dapat di-*save* pada saat ini, untuk kemudian di-*load* pada main menu.

> Jika subsistem Arduino menyala dan terkoneksi dengan komputer, maka data pada Arduino otomatis akan dikirim ke komputer. Subsistem Unity akan mengambil data ini yang kemudian dapat mempengaruhi permainan tergantung pada hasil pembacaan cuaca, apakah cuaca cerah atau tidak cerah.

> Jika subsistem Unity mendapatkan koneksi internet, maka subsistem Android dapat memesan barang ke subsistem Unity. Subsistem Unity juga dapat mengirimkan promo ke subsistem Android dengan menekan tombol *Send Promo* di kanan atas.

## Deliverables

- **Android**
Project : android
URL : http://gitlab.informatika.org/IF3111-2017-04/android
- **Unity**
Project : unity
URL : http://gitlab.informatika.org/IF3111-2017-04/unity
- **Arduino**
Project : arduino
URL : http://gitlab.informatika.org/IF3111-2017-04/arduino
- **API server**
Github : https://github.com/reinhardlinardi/mobile-inc

<br/>
<br/>© 2017, Chlordane. Mobile, Inc.™ is a registered trademark of Chlordane. All rights reserved.
<br/>Visit Mobile, Inc.™ homepage at http://mobileinc.herokuapp.com