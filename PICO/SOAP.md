# SOAP - Web Exploitation - Medium

## Description
The web project was rushed and no security assessment was done. Can you read the /etc/passwd file? 

## Hint
XML external entity Injection

## Solution

### 1.
Pertama kita buka web yang diberikan oleh PICOCTF, yaitu `http://saturn.picoctf.net:<port>/`, maka kita akan redirect ke sebuah website yang akan kita eksekusi.  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/SOAP/Screenshot%20From%202025-01-30%2010-45-10.png?raw=true)

### 2.
Setelah itu, kita buke Burpsuite untuk melakukan serangan XML external entity Injection `XEE Injection` pada website yang diberikan. nyalakan intercept dan lakukan aksi yang mentrigger keluarnya post request agar dapat dimasukkan ke repeater.  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/SOAP/Screenshot%20From%202025-01-30%2010-34-45.png?raw=true)

### 3. 
Setelah mendapatkan Post request, kita modifikasi pada bagian XML dengan `XEE`, saya mendapatkan cara melakukan [XEE Injection](https://portswigger.net/web-security/xxe) pada link disamping untuk melakukan serangan.  

![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/SOAP/Screenshot%20From%202025-01-30%2010-34-06.png?raw=true)  
Setelah itu, lakukan serangan dengan menambahkan line baru yang bertuliskan  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/SOAP/Screenshot%20From%202025-01-30%2010-51-55.png?raw=true)

### 4. 
Setelah memodifikasi bagian XML, maka repeater dijalankan dan mendapatkan hasil sebagai berikut. hasil tersebut merupakan XEE dan di dalamnya terdapat flag yang kita cari.  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/SOAP/Screenshot%20From%202025-01-30%2010-34-12.png?raw=true)

# THANKS!
