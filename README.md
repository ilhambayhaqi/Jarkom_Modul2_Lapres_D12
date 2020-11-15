# Jarkom_Modul2_Lapres_D12
- Muhammad Ilham Bayhaqi - 05111840000069
- Clever Dicki Marpaung - 05111840000116

# Solusi

### Soal 1
- Pada UML Malang dilakukan konfigurasi zone pada /etc/bind/named.conf.local sebagai berikut.
<img src=""></img>
- Melakukan copy pada file /etc/bind/db.local ke /etc/bind/jarkom/semerud12.pw
- Pada /etc/bind/jarkom/semerud12.pw dilakukan konfigurasi dengan record A mengarah ke IP Malang sebagai berikut.
<img src=""></img>
- Melakukan restart bind9 dengan ```service bind9 restart``` dan pada client ditambahkan nameserver IP Malang.
<img src=""></img>

### Soal 2
- Pada UML Malang, dilakukan konfigurasi pada file /etc/bind/jarkom/semerud12.pw ditambahkan record CNAME sebagai berikut.
<img src=""></img>
- Melakukan restart bind9 dengan  ```service bind9 restart```
<img src=""></img>

### Soal 3
- Pada UML Malang, dilakukan konfigurasi pada file /etc/bind/jarkom/semerud12.pw ditambahkan record untuk subdomain sebagai berikut.
<img src=""></img>
- Melakukan restart bind9 dengan  ```service bind9 restart```
<img src=""></img>

### Soal 4
- Pada UML Malang dilakukan konfigurasi zone untuk Reverse DNS pada /etc/bind/named.conf.local sebagai berikut.
<img src=""></img>
- Melakukan copy pada file /etc/bind/db.local ke /etc/bind/jarkom/79.151.10.in-addr.arpa
- Pada /etc/bind/jarkom/79.151.10.in-addr.arpa dilakukan konfigurasi untuk Reverse DNS nya menuju semerud12.pw.
<img src=""></img>
- Melakukan restart bind9 dengan ```service bind9 restart``` dan pada client ditambahkan nameserver IP Malang.
<img src=""></img>

### Soal 5
- Pada UML Malang dilakukan konfigurasi zone  pada /etc/bind/named.conf.local untuk dijadikan master sebagai berikut.
<img src=""></img>
- Dilakukan restart bind9 dengan ```service bind9 restart``` pada UML Malang.
- Pada UML Mojokerto dilakukan konfigurasi pada /etc/bind/named.conf.local untuk dijadikan slave sebagai berikut.
<img src=""></img>
- Dilakukan restart bind9 dengan ```service bind9 restart``` pada UML Mojokerto.

Untuk testing dilakukan ```service bind9 stop``` pada UML Malang.
<img src=""></img>

### Soal 6
- Pada UML Malang dilakukan konfigurasi pada /etc/bind/jarkom/semerud12.pw untuk melakukan delegasi name server pada IP Mojokerto.
<img src=""></img>
- Pada file /etc/bind/named.conf.options di UML Malang dilakukan comment untuk **dnssec-validation auto;** dan ditambahkan **allow-query{any;};**
- Pada file /etc/bind/named.conf.local dibuat konfigurasi seperti ini
<img src=""></img>
- Pada file /etc/bind/named.conf.options di UML Mojokerto dilakukan comment untuk **dnssec-validation auto;** dan ditambahkan **allow-query{any;};**

### Soal 7


### Soal 8
- Pertama, melakukan instalasi apache2 dan php5 pada server Probolinggo.
- Kemudian dilakukam download file dengan perintah wget 10.151.36.202/semeru.pw.zip dan hasil unzip semeru.pw dan di pindahkan menuju /var/www/semerud12.pw. 
- Untuk konfigurasinya maka dibuatkan file semerud12.pw pada direktori /etc/apache2/sites-available/semerud12.pw yang awalnya merupakan file copy dari file default.
- Isi konfigurasinya sebagai berikut.
<img src=""></img>
- Untuk mengaktifkan sitenya maka dilakukan perintah a2ensite semerud12.pw dan dilakukan restart pada Apache2.
<img src=""></img>

### Soal 9
### Soal 10
- Pertama, melakukan download file untuk penanjakan dengan perintah wget 10.151.36.202/penanjakan.semeru.pw.zip dan hasil unzipnya dipindakhan menuju /var/www/penanjakan.semerud12.pw.
- Untuk konfigurasinya dibuatkan file penanjakan.semerud12 pada direktori /etc/apache2/sites-available/penanjakan.semerud12.pw yang awalnya merupakan file copy dari file default.
- Untuk Konfigurasinya sebagai berikut.
<img src=""></img>
- Untuk mengaktifkan sitenya maka dilakukan perintah a2ensite semerud12.pw dan dilakukan restart pada Apache2.
<img src=""></img>

### Soal 11
- Karena pada folder /public dibolehkan directory listing  dan di dalamnya tidak maka dibuatkan konfigurasi sebagai berikut.
<img src=""></img>
- Agar konfigurasinya dijalankan maka dilakukan restart Apache2.
<img src=""></img>

### Soal 12
- Pada folder /errors disediakan page 404. Untuk mengubah page 404 default pada penanjakan.semerud12.pw, maka ditambahkan sebuah konfigurasi pada /etc/apache2/sites-available/penanjakan.semerud12.pw.
- Konfigurasinya sebagai berikut.
<img src=""></img>
- Agar konfigurasinya dijalankan maka dilakukan restart Apache2.
<img src=""></img>

### Soal 13
- Pada konfigurasi /etc/apache2/sites-available/penanjakan.semerud12.pw ditambahkan alias sebagai berikut.
<img src=""></img>
- Agar konfigurasinya dijalankan maka dilakukan restart Apache2.
<img src=""></img>

### Soal 14
- Pertama, melakukan download file untuk penanjakan dengan perintah wget 10.151.36.202/naik.gunung.semeru.pw.zip dan hasil unzipnya dipindakhan menuju /var/www/naik.gunung.semerud12.pw.
- Untuk konfigurasinya dibuatkan file penanjakan.semerud12 pada direktori /etc/apache2/sites-available/naik.gunung.semerud12.pw yang awalnya merupakan file copy dari file default.
- Agar hanya bisa diakses menggunakan port 8888 maka pada Virtual Host di set untuk port 8888.
- Untuk Konfigurasinya sebagai berikut.
<img src=""></img>
- Untuk mengaktifkan sitenya maka dilakukan perintah a2ensite semerud12.pw dan dilakukan restart pada Apache2.
<img src=""></img>

### Soal 15
- Pada Apache2-Utils terdapat fitur yang dapat digunakan untuk membuat user dengan htpasswd. Untuk membuat akun dengan nama "semeru", maka dilakukan dengan command sebagai berikut.
```
 htpasswd -c /etc/apache2/.htpasswd semeru
```
- Setelah dilakukan command tersebut, nanti akan ada perintah untuk meninputkan password. Password disi dengan "kuynaikgunung".
- Bila user berhasil dibuat maka pada file /etc/apache2/.htpasswd akan terlihat sebagai berikut.
<img src=""></img>
- Agar Authentikasi diterapkan maka ditambahkan konfigurasi pada file /etc/apache2/sites-available/naik.gunung.semerud12.pw sebagai berikut.
<img src=""></img>
- Agar konfigurasinya dijalankan maka dilakukan restart Apache2.
<img src=""></img>

### Soal 16
- Agar bila IP Probolinggo ketika dikunjungi mengarah ke semeru, maka pada /etc/apache2/sites-available/default ditambahkan konfigurasi sebagai berikut.
<img src=""></img>
- Agar konfigurasinya dijalankan maka dilakukan restart Apache2.
<img src=""></img>

### Soal 17




