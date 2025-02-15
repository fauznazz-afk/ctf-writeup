# Sql Direct - Web Exploitation - Medium

## Description
Connect to this PostgreSQL server and find the flag! "`psql -h saturn.picoctf.net -p 60472 -U postgres pico`" Password is "`postgres`"  

## Hint
What does a SQL database contain?  

## Solution  
![alt_text](?raw=true)

### 1.
Pertama kita connect postgresql server yang telah diberikan menggunakan terminal, lalu ketikkan `"\c"` untuk melhiat lokasi database sekarang, dan ketik `"\l"` untuk melihat list database yang tersedia  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/SQL_Direct/Screenshot%20From%202025-02-12%2022-43-10.png?raw=true)

### 2.
Ketik `"\d"` untuk melihat relation yang tersedia di dalam database dan ketik `"\dt flags"` untuk memasuki relasi yang tersedia di dalamnya.  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/SQL_Direct/Screenshot%20From%202025-02-12%2022-45-59.png?raw=true)  

### 3.  
Setelah itu kita dapat melakukan sql command, ketikkan `" select address from flags"` untuk melihat isi dari address, maka akan dapat flag yang diacri.  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/SQL_Direct/Screenshot%20From%202025-02-12%2022-46-20.png?raw=true)

# THANKS!

