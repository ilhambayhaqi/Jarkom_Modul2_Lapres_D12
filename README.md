# Jarkom_Modul2_Lapres_D12
- Muhammad Ilham Bayhaqi - 05111840000069
- Clever Dicki Marpaung - 05111840000116

# Solusi

### Soal 1
### Soal 2
### Soal 3
### Soal 4
### Soal 5
### Soal 6
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
### Soal 14
### Soal 15
### Soal 16
### Soal 17



