# secret - Web Exploitation - Medium

## Description
We have several pages hidden. Can you find the one with the flag? 

## Hint
folders folders folders 

## Solution  
![alt_text](?raw=true)

### 1.  
Klik website yang diberikan oleh PicoCTF maka akan diarahkan ke page halaman  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/Secret/Screenshot%20From%202025-02-15%2009-31-12.png?raw=true)  

### 2.  
Setelah itu kita lakukan inspect element, lihat pada bagian source lalu page, maka akan terlihat suatu url tersembunyi yaitu `"/secret"`, kita ketikkan pada belakang url menjadi `"url/secret/"`  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/Secret/Screenshot%20From%202025-02-15%2009-31-42.png?raw=true)  

### 3.  
Setelah mengetikkan url tadi, maka akan dialihkan ke halaman page baru, kita coba lagi untuk memasukkan url yang tersembunyi `"url/secret/hidden/"`  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/Secret/Screenshot%20From%202025-02-15%2009-32-04.png?raw=true)  

### 4.  
Setelah memasukkan url, maka akan dialihkan ke halaman page baru, kita masukkan lagi url yang tersembunyi selanjutnya `"url/secret/hidden/superhidden/"`   
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/Secret/Screenshot%20From%202025-02-15%2009-32-20.png?raw=true)  

### 5.  
Setelah dialihkan, kita akan melihat webpage yang kosong. lihat pada bagian source dan klik file superhidden, maka kita akan menemukan flag yang dicari  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/Secret/Screenshot%20From%202025-02-15%2009-32-34.png?raw=true)  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/Secret/Screenshot%20From%202025-02-15%2009-32-53.png?raw=true)

# THANKS!
