# No Sql Injection - Web Exploitation - Medium

## Description
Can you try to get access to this website to get the flag?  
You can download the source here.  
Additional details will be available after launching your challenge instance.  

## Hint
1. Not only SQL injection exist but also NonSQL injection exists.
2. Make sure you look at everything the server is sending back.

## Solution  

### 1. 
Download file yang telah diberikan oleh PICOCTF dan ekstrak, lalu lihat pada file server.js untuk mengetahui petujuk selanjutnya. di dapat bahwa server menggunakan mongoDB dimana merupakan Nosql database, maka dapat dilakukan injeksi Nosql. hal menarik lainnya adalah didapat sebuah email yang digunakan untuk login nantinya.  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/NoSql_Injection/Screenshot%20From%202025-01-30%2009-47-51.png?raw=true)

### 2.
Setelah itu, buka website yang telah di berikan oleh PICOCTF `http://atlas.picoctf.net:<port>/` dan gunakan email yang didapat. setelah itu gunakan Nosql injection pada kolom password.  
> #in URL  
username[$ne]=toto&password[$ne]=toto
username[$regex]=.*&password[$regex]=.*
username[$exists]=true&password[$exists]=true

> #in JSON  
{"username": {"$ne": null}, "password": {"$ne": null} }
{"username": {"$ne": "foo"}, "password": {"$ne": "bar"} }
{"username": {"$gt": undefined}, "password": {"$gt": undefined} }

![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/NoSql_Injection/Screenshot%20From%202025-01-30%2009-57-22.png?raw=true)

### 3.
Setelah login, maka akan redirect ke halaman admin, disini tampak biasa saja maka dari itu kita melakukan inspect element dan mencari ha yang menarik di dalamnya. Pada kolom `application`, di dalam session storage ditemukan sebuah token yang terenkripsi base64, ini menjadi indikasi sebuah flag.

![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/NoSql_Injection/Screenshot%20From%202025-01-30%2010-02-07.png?raw=true)

### 4.
Kita copy dan melakukan dekripsi dengan terminal. saya melakukan `echo "<token>" | base64 -d` untuk mendekripsi token tadi, maka di dapat sebuah flag yang dicari.  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/NoSql_Injection/Screenshot%20From%202025-01-30%2010-04-51.png?raw=true)

# THANKS!
