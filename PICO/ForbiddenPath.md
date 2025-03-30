# Forbidden Path - Web Exploitation - Medium

## Description
Can you get the flag?  
We know that the website files live in /usr/share/nginx/html/ and the flag is at /flag.txt but the website is filtering absolute file paths. Can you get past the filter to read the flag?
Source code can be downloaded here.  
Website can be accessed here!.  
![alt_text](?raw=true)
## Hint
-
## Solution  

### 1. 
Buka website yang diberikan oleh PicoCTF, dan akan tampil halaman berikut.  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/ForbiddenPath/Screenshot%20From%202025-03-30%2019-43-37.png?raw=true)

### 2.  
Situs web ini memiliki fitur yang berguna untuk membaca file apa pun yang kita inginkan, sesuai dengan jalurnya. Pada jalur berkas, ./ yang diawali dengan tanda ./ berarti direktori saat ini, dan ../ berarti direktori yang diapitnya. Karena kita tahu bahwa kita berada di /usr/share/nginx/html/, dan ingin mengakses /flag.txt, kita dapat menggunakan jalur ../../../../flag.txt untuk membaca flag.  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/ForbiddenPath/Screenshot%20From%202025-03-30%2019-43-54.png?raw=true)  

### 3. 
Maka akan dapat flag yang dicari  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/ForbiddenPath/Screenshot%20From%202025-03-30%2019-44-01.png?raw=true)

