# SQLiLITE - Web Exploitation - Medium

## Description
CCan you login to this website?

## Hint
admin is the user you want to login.

## Solution  

### 1.
Pertama, ke website yang telah diberikan oleh PICOCTF, yaitu `http://saturn.picoctf.net:<port>/login.php`, lalu akan muncul tampilan web sebagai berikut.  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/SQLiLITE/Screenshot%20From%202025-01-30%2019-56-31.png?raw=true)

### 2.
Setelah masuk, kita akan menjalankan [SQL Injection](https://portswigger.net/web-security/sql-injection#what-is-sql-injection-sqli) pada halaman login tersebut, saya memasukkan  
> username = admin  
> password = ' or '1' = '1' --  

untuk mendapatkan  akses ke dalam halaman selanjutnya.  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/SQLiLITE/Screenshot%20From%202025-01-30%2019-56-58.png?raw=true)

### 3.
Setelag redirect ke halaman selanjutnya, maka akan muncul hint baru, yaitu **"Logged in! But can you see the flag? it is in plainsight"**, yang dimana artinya saya harus melakukan inspect elemen.  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/SQLiLITE/Screenshot%20From%202025-01-30%2019-57-11.png?raw=true)  

### 4.  
Setelah melakukan inspect elemen, saya mencari pada bagian **"Logged in! But can you see the flag? it is in plainsight"** dan memperbesarnya, maka di dapat flag yang di cari.  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/SQLiLITE/Screenshot%20From%202025-01-30%2019-57-25.png?raw=true)  

# THANKS!
