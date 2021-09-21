# Praktikum5
## Pengantar
Praktikum 5 ini terdiri dari 2 bagian. Bagian pertama berisi Modul 1 dan bagian kedua berisi Modul 2. Bagian pertama ini dikerjakan selama sesi praktikum, sementara bagian kedua dikerjakan pada jam mandiri.
Deadline penyetoran untuk masing-masing bagian diset berbeda, informasi deadline dan link bagian II akan disampaikan terpisah.

**Inheritance** adalah konsep di mana kelas anak (sub class/child class/derived class) mewarisi semua atribut dan method yang public/protected dari kelas bapak (superclass/parent class/base class).
Atribut atau method yang diwarisi dari kelas bapak, tidak ditulis di dalam kelas anak, tapi objek dari kelas anak memiliki dan dapat memanggil method yang diwariskan oleh bapak.

## Petunjuk Praktikum
Baca instruksi yang diberikan dengan baik.

#### Modul 1 **[Poin 30]** Kelas Binatang dan turunannya serta kelas Driver.
Berikut adalah diagram kelas Binatang yang sudah saya jelaskan di video pembelajaran pada sesi asinkronus minggu ini.

![Image of Gbr5.1](https://apipuro.del.ac.id/v1/file/9c99743a4040f937b3e52d5561cb7b6d)

Pada kelas diagram di atas, dapat dilihat adanya konsep inheritance/pewarisan (ditandai dengan tanda panah tertutup dari subclass ke superclass). Kelas Binatang menjadi superclass, sementara kelas Ayam, Anjing dan Kucing adalah subclass dari kelas Binatang. 
Subclass Ayam, Anjing dan Kucing mewarisi **semua atribut dan method yang tidak diberi modifier private** dari kelas Binatang.

***Modul 1.a*** Berikut ini adalah kode program hasil implementasi diagram kelas di atas. Tulis ulang semua kode program berikut ini dan simpan di dalam folder src\main\java. Jika penulisan anda benar maka anda akan mendapat nilai full untuk testDriver.

>**Kelas Binatang.java**
![Image of Gbr5.2.a](https://apipuro.del.ac.id/v1/file/902511ddcc61fe078d06e1cbc20fcd6a)
![Image of Gbr5.2.b](https://apipuro.del.ac.id/v1/file/4c22f9e32cde23817646d9090b3dd58a)

>**Kelas Anjing.java**
![Image of Gbr5.2.a](https://apipuro.del.ac.id/v1/file/493d5c82d5664fdc057a47b6ae95140b)

>**Kelas Ayam.java**
![Image of Gbr5.2.b](https://apipuro.del.ac.id/v1/file/dc2fda8aa0bc155503433aa713a679d6)

>**Kelas Kucing.java**
![Image of Gbr5.2.c](https://apipuro.del.ac.id/v1/file/3444b2c418ee93ce6395024c8228d13c)

>**Kelas Driver.java**
![Image of Gbr5.2.d](https://apipuro.del.ac.id/v1/file/8a2c13a8e46477491f8de7ac4a7a1043)
 
 Perhatikan hasil eksekusi program Driver.java, suara Garfield masih salah. Perbaiki kode program Driver.java, supaya Garfield mengeluarkan suara kucing.
 
 
 ***Modul 1.b*** Misalkan ada kebutuhan untuk menyimpan posisi kucing, sehingga atributnya perlu ditambah dengan variabel bertipe Point yang akan menyimpan data posisi. Sementara method bergerak yang diwarisi oleh kelas Kucing hanya mengembalikan sebuah string. Kelas Kucing membutuhkan method bergerak yang dapat mengubah posisi kucing pada koordinat x dan y. Oleh karena itu, kelas Kucing diubah dengan menambahkan atribut posisi, mengupdate constructor, menambah setter/getter untuk posisi, dan **membuat variasi lain dari method bergerak/overloading**. Definisi method bergerak lain yang dibutuhkan kelas Kucing adalah sebagai berikut:
	
	bergerak (jmlLangkah:int, arah:string) : string
	parameter jmlLangkah menyatakan jumlah langkah
	parameter arah menerima salah satu dari nilai maju, mundur, kiri atau kanan. Arah maju atau mundur akan mengupdate posisi pada sumbu ordinat, sementara kiri dan kanan akan mengupdate posisi pada sumbu absis.
Modifikasi kelas Kucing.java sesuai dengan kode program berikut ini (kotak merah adalah bagian yang diubah/ditambah pada kelas Kucing). Salin ulang kelas Driver yang sudah dimodifikasi untuk memanggil kelas Kucing yang baru. Perhatikan bahwa kelas Kucing memiliki dua method bergerak(). Method mana yang akan digunakan akan tergantung pada cara pemanggilannya.

>Kelas Kucing.java
![Image of Gbr5.2.e](https://apipuro.del.ac.id/v1/file/c95ec885abb54b46de048c1cde716123)
![Image of Gbr5.2.f](https://apipuro.del.ac.id/v1/file/87e2babdab4ab6b7fdb576f454638e63)

>Kelas Driver.java
![Image of Gbr5.2.g](https://apipuro.del.ac.id/v1/file/a31627c7f2bf4cc4d8a30f23208609d1)

***Modul 1.c*** Ayam secara khusus makan dengan cara mematuk. Oleh karena itu method makan() yang diwarisinya tidak sesuai dan perlu **ditulis ulang/dioverride**.
Modifikasi kelas Ayam.java sesuai dengan kode program berikut ini. Jalankan ulang kode program Driver.java, screenshot hasil eksekusi Driver.java sebelum dan sesudah modifikasi kelas Ayam.java dan upload pada laporan praktikum 5 di ecourse. Tandai bagian yang berubah setelah dilakukan modifikasi.
Perhatikan bahwa kelas Ayam hanya memiliki satu method makan() yaitu method yang ditulis di dalam kelas Ayam() dan bukan yang diwariskan oleh kelas Binatang.
>Kelas Ayam.java
![Image of Gbr5.2.h](https://apipuro.del.ac.id/v1/file/b860fe35e479992bf815282f2ddc4de7)



**Catatan Penting:**
1. Anda hanya boleh mengubah kode program yang ada di src\main\java
1. **Semua kode program yang ada di src\test\java  tidak boleh diubah sama sekali!!** Jika anda ubah (akan terlihat pada history), maka nilai anda langsung 0.
1. Jangan memindah-mindahkan file, biarkan setiap file di folder di mana file tersebut berada sebelumnya.
1. Pada beberapa template program sudah disediakan method yang tidak boleh diubah. Maka jangan anda ubah!
