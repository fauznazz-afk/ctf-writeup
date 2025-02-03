# MatchTheRegex - Web Exploitation - Medium
![alt_text](?raw=true)

## Description
How about trying to match a regular expression The website is running here (http://saturn.picoctf.net:<port>/)  

## Hint
Access the webpage and try to match the regular expression associated with the text field  

## Solution

### 1.
Kunjungi halaman yang diberikan oleh PICOCTF, yaitu `(http://saturn.picoctf.net:<port>/) `, setelah redirect maka akan muncul halaman untuk memasukkan valid input.  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/MatchTheRegex/Screenshot%20From%202025-02-03%2016-00-52.png?raw=true)


#### 2.  
Saya mencoba mengetikkan huruf random dan melakukan submit, tetapi ternyata salah dan harus mencari cara lain untuk mendapatkan flagnya.  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/MatchTheRegex/Screenshot%20From%202025-02-03%2016-01-07.png?raw=true)  

#### 3.
Selanjutnya melakukan Inspect Element untuk memabaca kode yang ada di dalamnya, saya menemukan sebuah script dimana Skrip ini mengambil input pengguna dari bidang formulir, mengirimkannya ke skrip sisi server di endpoint /flag, menerima respons JSON, mengekstrak nilai flag dari respons tersebut, dan menampilkan nilai flag dalam kotak alert pop-up.  
Pada bagian `// ^p.....F!?` merupakan sebuah hint dimana regex yang tepat adalah yang berawalan **"p"** dan berakhiran **"F!"**, maka saya copy line tersebut untuk dimasukkan ke dalam formulir.  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/MatchTheRegex/Screenshot%20From%202025-02-03%2016-01-33.png?raw=true)  

#### 4.
Setelah saya paste dan submit, maka flag yang dicari akan keluar.  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/MatchTheRegex/Screenshot%20From%202025-02-03%2016-02-12.png?raw=true)  

# THANKS!
