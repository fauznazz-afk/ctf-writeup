# Java Code Analysis!?! - Web Exploitation - Medium

## Description
BookShelf Pico, my premium online book-reading service. I believe that my website is super secure. I challenge you to prove me wrong by reading the 'Flag' book!  
Here are the credentials to get you started:
> Username: "user"  
> Password: "user"

Source code can be downloaded here.
Website can be accessed here!.  

## Hint
1. Maybe try to find the JWT Signing Key ("secret key") in the source code? Maybe it's hardcoded somewhere? Or maybe try to crack it?
2. The 'role' and 'userId' fields in the JWT can be of interest to you!
3. The 'controllers', 'services' and 'security' java packages in the given source code might need your attention. We've provided a README.md file that contains some documentation.  
4. Upgrade your 'role' with the new (cracked) JWT. And re-login for the new role to get reflected in browser's localStorage.  

![alt_text](?raw=true)
## Solution  

#### 1.  
Pertama masuk dengan credentials yang telah di berikan oleh PICOCTF, lalu download file yang diberikan.
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/JavaCodeAnalysis/Screenshot%20From%202025-01-31%2009-06-54.png?raw=true)

### 2.  
Setelah itu, baca hint yang diberikan, lakukan inspect element dan cari pada kolom storage untuk mendapatkan JWT Signing key, lihat pada `role` dan `userId` karena dua hal tersebut sangat menarik dimana kedua fields tersebut menentukan akses dan identifikasinya.  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/JavaCodeAnalysis/Screenshot%20From%202025-01-31%2009-07-32.png?raw=true)

### 3. 
Pada petunjuk selanjutnya, kita harus mencari file yang di dalamnya terdapat `controllers`, `services` and `security`, setelah di cari saya menemukan hal menarik, dimana pada gambar tersebut, akses pada buku yang bertuliskan **FLAG** harus dapat akses admin untuk membukanya. 
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/JavaCodeAnalysis/Screenshot%20From%202025-01-31%2009-09-01.png?raw=true)  
Pada gambar kedua, saya mendapatkan akses dari `VERIFY SIGNATURE` untuk JWT yang akan dimodifikasi nantinya yaitu **1234**
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/JavaCodeAnalysis/Screenshot%20From%202025-01-31%2009-09-15.png?raw=true)

### 4.
Setelah mendapatkan JWT pada step 2, maka buka [JWT.io](JWT.io) untuk memodifikasi JWT yang telah di dapatkan melalui inspect element. Pada bagian payload, kita modifikasi roles = Admin, UserId = 2, `karena semakin tinggi angka, semakin tinggi akses` dan email = admin. Setelah editing, copy pada bagian encoded agar kita modifikasi di JWT web PICOCTF

![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/JavaCodeAnalysis/Screenshot%20From%202025-01-31%2008-38-19.png?raw=true)

### 5.
Kita ubah di Auth-token dengan encode yang kita dapat, serta modifikasi token payload, ubah menjadi roles = Admin, UserId = 2, dan email = admin untuk mesinkron antara Auth-key dan token payload.  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/JavaCodeAnalysis/Screenshot%20From%202025-01-31%2009-07-32.png?raw=true)

### 6. 
Setelah itu refresh page, dan akses pada buku **"FLAG"**, maka akan didapat flag yang dicari.  
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/JavaCodeAnalysis/Screenshot%20From%202025-01-31%2009-08-24.png?raw=true)

# THANKS!
