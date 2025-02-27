# Search Source - Web Exploitation - Medium

## Description
The developer of this website mistakenly left an important artifact in the website source, can you find it?  
  
## Hint
How could you mirror the website on your local machine so you could use more powerful tools for searching?   

## Solution  
![alt_text](?raw=true)  
### 1.
Kita buka link yang diberi oleh picoCTF dan akan dialihkan ke sebuah website.
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/searchsource/Screenshot%20From%202025-02-27%2019-42-28.png?raw=true)  

### 2.
Mengacu pada hint yang diberikan, maka kita clone dulu web tersebut dengan menggunakan command `"wget --mirror http://saturn.picoctf.net:50079/
"` agar kita dapat mengetahui letak flag yang dicari  

![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/searchsource/Screenshot%20From%202025-02-27%2019-42-40.png?raw=true) 

### 3.
Setelah melakukan cloning, kita mendapatkan folder yang berjudul `"saturn.picoctf.net:50079"`, kita msuk ke folder dengan mengetikkan `"cd saturn.picoctf.net:50079"` lalu kita cek file yang terdapat di dalam folder tersebut  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/searchsource/Screenshot%20From%202025-02-27%2019-43-22.png?raw=true)  

### 4.
Karena ada banyak file di dalam folder tersebut, kita tidak mungkin mengecek satu per satu, maka kita gunakan `grep` untuk memudahkan mencari flag, ketik `"grep -r pico"` untuk mencari flag yang tersembunyi dengan cepat.  

![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/searchsource/Screenshot%20From%202025-02-27%2019-41-17.png?raw=true)  

Maka flag yang dicari akan muncul  


# THANKS

