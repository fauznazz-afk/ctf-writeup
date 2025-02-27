# Roboto Sans - Web Exploitation - Medium

## Description
The flag is somewhere on this web application not necessarily on the website. Find it. 

## Hint
None
![alt_text](?raw=true)

## Solution

### 1.
Kita masuk ke dalam link yang diberikan oleh picoCTF dan akan muncul laman web sebagai berikut.  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/RobotSans/Screenshot%20From%202025-02-27%2021-00-59.png?raw=true)
Karena tidak adanya clue, maka saya akan menambahkan **/robots.txt** pada url web. fungsi robots.txt sendiri adalah file teks yang berisi instruksi untuk bot mesin pencari, seperti Google. File ini mengatur apakah bot boleh mengakses halaman tertentu di situs web.  

### 2. 
Setelah masuk ke **/robots.txt**, maka akan terlihat url-url yang tersedia, ada beberapa yang terenkripsi oleh base64, maka kita akan dekripsi url tersebut  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/RobotSans/Screenshot%20From%202025-02-27%2021-01-17.png?raw=true)   
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/RobotSans/Screenshot%20From%202025-02-27%2021-03-06.png?raw=true)  

### 3.
Setelah melakukan dekripsi, maka akan menemukan kembali url yang menarik, yaitu **js/myfile.txt**, maka kita ketik url yang dibelakangnya **js/myfile.txt** seperti gambar di bawah ini.  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/RobotSans/Screenshot%20From%202025-02-27%2021-03-33.png?raw=true)  
Setelah diketik, maka kita akan mendapatkan flag yang dicari.

# THANKS

