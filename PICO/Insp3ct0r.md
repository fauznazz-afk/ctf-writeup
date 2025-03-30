# Insp3ct0r- Web Exploitation - Easy

## Description
Kishor Balan tipped us off that the following code may need inspection: https://jupiter.challenges.picoctf.org/problem/9670/ (link) or http://jupiter.challenges.picoctf.org:9670

Source code can be downloaded here.
Website can be accessed here!.  

## Hint
1. How do you inspect web code on a browser?
2. There's 3 parts
![alt_text](?raw=true)

## Solution

### 1.  
Pertama, buka link yang diberkan lalu lakukan inspect elemen pada web untuk melihat flag
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/Insp3ct0r/Screenshot%20From%202025-03-30%2021-00-31.png?raw=true)
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/Insp3ct0r/Screenshot%20From%202025-03-30%2021-00-46.png?raw=true)

### 2.  
Dapat dilihat, kita mendapatkan bagian 1, kita lihat pada bagian source untuk mendapatkan bagian yang lainnya
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/Insp3ct0r/Screenshot%20From%202025-03-30%2021-01-41.png?raw=true)
![alt_text](https://github.com/fauznazz-afk/ctf-writeup/blob/main/Documentation/Insp3ct0r/Screenshot%20From%202025-03-30%2021-01-48.png?raw=true)

### 3.  
maka didapat flagnya **picoCTF{tru3_d3t3ct1ve_0r_ju5t_lucky?832b0699}**

