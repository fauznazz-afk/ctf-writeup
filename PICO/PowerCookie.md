# Power Cookie - Web Exploitation - Medium

## Description
Can you get the flag?


## Hint
Do you know how to modify cookies?

## Solution  

### 1.
Pertama kita ke web yang diberi oleh picoCTF, dan akan tampil halaman seperti berikut. disini tidak ada apa-apa selain tomobol conitinue as guest  
[alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/PowerCookie/Screenshot%20From%202025-03-08%2009-25-18.png?raw=true)

### 2.
Setelah tomobol dipencet, maka akan dialihkan ke halaman ini, tidak ada flag yang tersedia di halaman web tersebut. maka kembali lagi ke halaman sebelumnya untuk melihat hint yang ada.  
[alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/PowerCookie/Screenshot%20From%202025-03-08%2009-26-26.png?raw=true)

### 3.
Kita coba inspect element, dan akan muncul sebuah hint, yaitu **guest.js**. dapat dilihat bahwa **document.cookie = IsAdmin=0**, inilah yang harus kita ubah agar mendapatkan akses admin dengan cara mengubah valuenya menjadi 1.  
[alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/PowerCookie/Screenshot%20From%202025-03-08%2009-27-01.png?raw=true)

### 4.
Kita pergi ke halaman cookies dan kita ubah cookies valuenya yang awalnya **0** menjadi **1**.  
[alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/PowerCookie/Screenshot%20From%202025-03-08%2009-27-22.png?raw=true)
[alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/PowerCookie/Screenshot%20From%202025-03-08%2009-27-30.png?raw=true)

### 5. 
Maka akan terlihat flag yang kita cari.  
[alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/PowerCookie/Screenshot%20From%202025-03-08%2009-28-07.png?raw=true)  

# THANKS!




