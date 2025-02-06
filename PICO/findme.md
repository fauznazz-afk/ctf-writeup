# findme - Web Exploitation - Medium

## Description
Help us test the form by submiting the username as `"test"` and password as `"test!"`
  
## Hint
Any redirections?  

## Solution  

### 1. 
Pertama buka web yang diberikan dan login menggunakan username dan password yang telah diberikan.
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/findme/Screenshot%20From%202025-02-06%2012-20-01.png?raw=true)  

### 2. 
Buka burpsuite,lakukan intercept dan lakukan forward pada bagian post request yang dihasilkan pada saat login  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/findme/Screenshot%20From%202025-02-06%2012-20-57.png?raw=true)  

### 3.
Setelah melakukan forward, lihat pada response yang diberikan. pada line 8 terdapat sebuah kata yang terenkripsi base64, namun itu hanya setengah dari flag yang kita cari. maka kita lakukan hal yang sama pada percobaan nomor dua, yaitu melakukan forward pada halaman selanjutnya. 
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/findme/Screenshot%20From%202025-02-06%2012-21-43.png?raw=true)    

![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/findme/Screenshot%20From%202025-02-06%2012-21-53.png?raw=true)  

### 4.
Setelah menemukan bagian yang lengkap, maka saatnya didekripsi menggunakan base64  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/findme/Screenshot%20From%202025-02-06%2012-22-41.png?raw=true)    
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/findme/Screenshot%20From%202025-02-06%2012-22-52.png?raw=true)   

Maka kita dapatkan flag yang kita cari.

# THANKS!
