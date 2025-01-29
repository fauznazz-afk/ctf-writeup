# Trickster - Web Exploitation

## Description
I found a web app that can help process images: PNG images only!  

## Hint
None

## Solution
### 1. 
Kunjungi website instance yang diberikan oleh PICOCTF, yaitu `http://atlas.picoctf.net/<port>`  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/PICO/Screenshot%20From%202025-01-29%2013-14-02.png?raw=true)


### 2. 
Langkah pertama yang dilakukan adalah dengan mencari direktori tersembunyi dengan metode enumerasi  
menggunakan `Gobuster` terhadap website ini `http://atlas.picoctf.net/<port>` dengan mengeksekusi perintah
`gobuster dir -u http://atlas.picoctf.net/<port> -w /usr/share/dirb/wordlists/common.txt`  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/PICO/Screenshot%20From%202025-01-29%2013-11-57.png?raw=true)

#### 3. 
Selanjutnya didapat direktori tersembunyi, yaitu `/robots.txt`, direktori ini yang akan kita cari di website sebelumnya 
setelah dicari maka akan didapat dua direktori tambahan yaitu `/instruction.txt` dan `/uploads/`, maka kita cari kembali untuk `/instruction.txt`  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/PICO/Screenshot%20From%202025-01-29%2013-12-15.png?raw=true)

### 4.  
Setelah ditelusuri, maka akan terlihat sebuah instruksi, maka yang perlu dilakukan adalah mengupload **webshell.php** agar mendapatkan akses untuk menjelajahi direktori web tersebut
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/PICO/Screenshot%20From%202025-01-29%2013-12-31.png?raw=true)

### 5  
Lalu saya mencari sebuah webshell.php di github untuk selanjutnya di upload di website sebelumnya. saya menggunakan code [webshell.php](https://github.com/drag0s/php-webshell/blob/master/webshell.php) dan mengubah sedikit code di dalamnya dengan menambahkan **PNG** pada bagian atas kode agar bisa terbaca saat upload nantinya.
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/PICO/Screenshot%20From%202025-01-29%2014-16-43.png?raw=true)

### 6  
Setelah itu, ubah nama file menjadi `webshell.png.php` dan upload ke website  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/PICO/Screenshot%20From%202025-01-29%2013-14-02.png?raw=true)

### 7   
Selanjutnya ketik `http://atlas.picoctf.net:<port>/uploads/webshell.png.php` untuk mengakses webshell yang telah ditanamkan sebelumnya   
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/PICO/Screenshot%20From%202025-01-29%2014-23-47.png?raw=true)

### 8  
Lalu ketik pada kolom pencarian **"/"** untuk menuju akar pada direktori. lalu scroll ke bawah hingga menemukan file yang bertuliskan **var/wwww/html/FHFQWKODGMIYTO.txt**  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/PICO/Screenshot%20From%202025-01-29%2013-19-42.png?raw=true)

### 9  
Ketik `cat var/wwww/html/FHFQWKODGMIYTO.txt` pada kolom execution dan pencet enter, maka file flag akan ditemukan.  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/PICO/Screenshot%20From%202025-01-29%2013-20-14.png?raw=true)

# THANKS!



