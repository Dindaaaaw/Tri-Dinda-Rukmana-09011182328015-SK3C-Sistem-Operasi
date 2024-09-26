TUGAS PRAKTIKUM 6 SISTEM OPERASI, JOB CONTROL

Nama : Tri Dinda Rukmana

Nim : 09011182328015

Kelasm: SK3C

1. Eksekusi seluruh profil yang ada:
   a. Edit file profil /etc/profile dan tampilkan pesan sebagai berikut:
echo “Profile dari /etc/profile”

![1 a](https://github.com/user-attachments/assets/c887a0cc-e6af-4d12-aba7-2e8660dad38b)

![1 a(1)](https://github.com/user-attachments/assets/32dd88a0-6459-46e6-8fec-84b6fdda1cee)

   b. Asumsi nama Anda stD02001, maka edit semua profil yang ada yaitu:

   /home/stD02001/.bash_profile

   /home/.stD02001/.bash_login

   /home/mahasiswa/.profile

   /home/mahasiswa/.bashrc

Ganti nama /home/mahasiswa dengan nama anda sendiri. Pada setiap file tersebut, cantumkan instruksi echo, misalnya pada 

/home/mahasiswa/.bash_profile :

echo “Profile dari .bash_profile”

Lakukan hal yang sama untuk file lainnya, sesuaikan tampilan dengan nama file yang bersangkutan.

![1 b](https://github.com/user-attachments/assets/ce87d378-ce43-4b71-b353-ba84f60588da)

![1 b(1)](https://github.com/user-attachments/assets/b52d1462-6ab2-46e6-a913-7c5924c0e262)

![1 b(2)](https://github.com/user-attachments/assets/19eec6c9-fb68-470b-ba4a-f4ca5a67923d)

![1 b(3)](https://github.com/user-attachments/assets/4a7a71ed-ec76-4f7b-952c-41249243eb10)

![1 b(4)](https://github.com/user-attachments/assets/0f770fd2-08b0-436f-8c83-9b7f64a777c2)

c. Jalankan instruksi subtitute user, kemudian keluar dengan perintah exit sebagai berikut:

$ su mahasiswa 

$ exit

![1 c(1)](https://github.com/user-attachments/assets/73e8f58b-8744-4c46-8581-11bf78e8ff78)

kemudian gunakan opsi – sebagai berikut :

$ su – mahasiswa

$ exit

![1 c(2)](https://github.com/user-attachments/assets/86692398-a7a1-4e1a-870b-d2cc54695dff)

Jelaskan perbedaan kedua utilitas tersebut.

su mahasiswa:
Perintah su mahasiswa digunakan untuk beralih ke akun pengguna bernama "mahasiswa" tanpa mengubah lingkungan shell secara penuh. Dalam hal ini, hanya identitas pengguna yang berubah, tetapi variabel lingkungan (seperti $PATH, alias, dan pengaturan shell lainnya) tetap milik pengguna saat ini. Ini berarti beberapa program atau perintah mungkin tidak berfungsi dengan benar karena masih menggunakan konfigurasi dari pengguna asli.


su - mahasiswa:
Sedangkan su - mahasiswa tidak hanya mengubah identitas pengguna, tetapi juga memulai sesi shell baru seperti halnya ketika pengguna "mahasiswa" masuk secara langsung. Semua variabel lingkungan akan direset sesuai dengan pengaturan default pengguna "mahasiswa", termasuk $HOME, $PATH, dan lainnya. Ini memberikan pengalaman yang lebih lengkap dan aman, seolah-olah Anda baru saja login sebagai "mahasiswa"


2. Prompt String (PS)

   a. Edit file .bash_profile, ganti prompt PS1 dengan ‘>’. Instruksi export diperlukan dengan parameter nama variable tersebut, agar perubahan variable PS1 dikenal oleh semua shell

   PS1=‟> „

   export PS1

![2 a1](https://github.com/user-attachments/assets/bf8f4d13-b31a-4418-9934-a988c4b710f8)

![2 a](https://github.com/user-attachments/assets/223cdd81-7c48-4a8e-a1bb-c37b70776da7)

   b. Eksperimen hasil PS1 :
   
   $ PS1=“! > “

   69 > PS1=”\d > “

   Mon Sep 23 > PS1=”\t > “

   10:10:20 > PS1=”Saya=\u > “

   Saya=mahasiswa > PS1=”\w >”

   ~ > PS1=\h >”
   
![2 b](https://github.com/user-attachments/assets/5e9dc2a0-31f8-4157-9d69-0cf934b6e580)

3. Logout

      Edit file .bash_logout, tampilkan pesan dan tahan selama 5 detik, sebelum eksekusi logout

      Echo “Terima kasih atas sesi yang diberikan”

      Sleep 5

      clear

![3 2](https://github.com/user-attachments/assets/38b77293-279e-4af2-9cfa-be3813e7c248)

![3 1](https://github.com/user-attachments/assets/d5ce2d36-32d4-4adf-90cc-d2f3f852a322)

4. Bash script

   a. Buat 3 buah script p1.sh, p2.sh, p3.sh dengan isi masing-masing :

   p1.sh

   #! /bin/bash

   echo “Program p1”

   ls –l

   p2.sh

   #! /bin/bash

   echo “Program p2”

   who

   p3.sh

   #! /bin/bash

   echo “Program p3”

   ps x

![4 a](https://github.com/user-attachments/assets/8f0d8fe4-d8ab-4d72-9611-43c27d862164)

![4 a(1)](https://github.com/user-attachments/assets/1377c657-4d74-443c-b576-3f6d50b6d1e2)

![4 a,a](https://github.com/user-attachments/assets/87d0256f-b443-42eb-903b-3cad177a4a10)

![4 a(2)](https://github.com/user-attachments/assets/126790a9-5fed-40e0-a7aa-18fd79c357ea)

![4 a(3 3)](https://github.com/user-attachments/assets/07b999da-293a-4719-b379-296b2c89a722)

![4 a(3)](https://github.com/user-attachments/assets/ee71a2e1-380a-4c30-bb68-90ef773bc6aa)

   b. Jalankan script tersebut sebagai berikut :

   $ ./p1.sh ; ./p3.sh ; ./p2.sh

   $ ./p1.sh &

   $ ./p1.sh $ ./p2.sh & ./p3.sh &

   $ ( ./p1.sh ; ./p3.sh ) &

![4 b(1)](https://github.com/user-attachments/assets/56833afe-1f34-4a50-b7ea-5fb5f13cdd85)

![4 b(2)](https://github.com/user-attachments/assets/310c0698-735e-45dc-94cd-c645a67c3f91)

![4 b(3)](https://github.com/user-attachments/assets/483f75a4-efe4-496b-b83c-793e59015387)

![4 b(1,1)](https://github.com/user-attachments/assets/ccd2b1cc-ed49-46c2-9ded-96490641c98f)

![4 b(1,2)](https://github.com/user-attachments/assets/beff23fb-2940-4bfd-90c4-4972eb1281f1)

![4 b(1,2 2)](https://github.com/user-attachments/assets/b7dd74e0-bb63-49ef-8a0c-0f43b45ae57f)

![4 b(1,3)](https://github.com/user-attachments/assets/119b423a-6625-42a8-91b0-3a6b323999a7)

![4 b(1,3 3)](https://github.com/user-attachments/assets/8dba9a91-3a4d-4c0d-a4a1-f3c26a1982c1)

5. Jobs
      
      a. Buat shell-script yang melakukan loop dengan nama pwaktu.sh, setiap 10 detik, kemudian menyimpan tanggal dan jam pada file hasil.

   #!/bin/bash

   while [ true ]

   do

   date >> hasil

   sleep 10

   done

![5 a](https://github.com/user-attachments/assets/2d18fa0e-f9ec-4ff1-8d82-3b6a73eacf3b)

![5 a(1)](https://github.com/user-attachments/assets/9b86e8f8-864b-431e-a929-0e15576e395a)

   b. Jalankan sebagai background; kemudian jalankan satu program (utilitas find) di background sebagai berikut :

   $ jobs

   $ find / -print > files 2>/dev/null &

   $ jobs

![5 b(1)](https://github.com/user-attachments/assets/bc17e149-4ab7-4f01-8ff0-840c89357990)

![5b](https://github.com/user-attachments/assets/b7f9ef43-2fd2-49c0-ab58-d53af5199faa)

   c. Jadikan program ke 1 sebagai foreground, tekan ^Z dan kembalikan program tersebut ke background

   $ fg %1

   $ bg

![5 c](https://github.com/user-attachments/assets/740f83aa-02b8-4739-9f30-875810e28947)

   d. Stop program background dengan utilitas kil

   $ ps x

   $ kill [Nomor PID]
   
![5 d(1)](https://github.com/user-attachments/assets/2b58cb0f-0361-43a9-a243-3dbf2842a21d)

![5 d(2)](https://github.com/user-attachments/assets/305a09b1-c649-498e-9cd8-7b2b035a1020)

6. History

   a. Ganti nilai HISTSIZE dari 1000 menjadi 20

   $ HISTSIZE=20

   $ h
   
![6 a(1)](https://github.com/user-attachments/assets/9c1562e5-94cd-45c7-b50a-2872adbc2d73)

![6 a(2)](https://github.com/user-attachments/assets/449cd66a-0bf5-439e-8612-ab521379a911)

   b. Gunakan fasilitas history dengan mengedit instruksi baris ke 5 dari instruksi yang terakhir dilakukan

   $ !-5
   
![6 b](https://github.com/user-attachments/assets/cdfe1b74-5f69-4c43-ba89-e41a5c8c6718)

   c. Ulangi instruksi yang terakhir. Gunakan juga ^P dan ^N untuk bernavigasi pada history bufer

   $ !!

![6 c](https://github.com/user-attachments/assets/e9ea9327-3e8d-4b20-bd4f-01c8b976ae06)

   d. Ulangi instruksi pada history bufer nomor 150

   $ !150

![6 d](https://github.com/user-attachments/assets/30d75087-6bd7-4d10-aa73-57c01d8173ee)

   e. Ulangi instruksi dengan prefix “ls”

   $ !ls

![6 e](https://github.com/user-attachments/assets/3891617a-4b51-4d3b-baf9-57a3cfcd4a66)






















