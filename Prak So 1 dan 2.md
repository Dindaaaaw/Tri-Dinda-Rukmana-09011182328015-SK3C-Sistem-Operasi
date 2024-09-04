# LAPORAN PRAKTIKUM PROSES INSTALASI SISTEM OPERASI LINUX

Disusun oleh:  

**Nama**: Tri Dinda Rukmana  
**NIM**: 09011182328015  
**Kelas**: SK3C  
**Mata Kuliah**: Sistem Operasi

## PROGRAM STUDI SISTEM KOMPUTER  
FAKULTAS ILMU KOMPUTER  
UNIVERSITAS SRIWIJAYA  
2024  

---

## BAB 1: PENDAHULUAN

### 1.1 Latar Belakang

Sistem Operasi komputer adalah perangkat lunak komputer atau software yang bertugas untuk melakukan kontrol dan manajemen perangkat keras dan juga operasi-operasi dasar sistem, termasuk menjalankan software aplikasi seperti program-program pengolah data yang bisa digunakan untuk mempermudah kegiatan manusia. Pada saat ini hampir semua orang menggunakan sistem operasi Windows sebagai sistem operasi di komputer mereka. Namun, sudah tahukah Anda dengan Sistem Operasi Linux? Memang tak bisa dipungkiri bahwa sebagian besar masyarakat Indonesia masih mengalami kesulitan dalam menguasai teknologi. Hanya sebagian kecil yang memiliki pemahaman mendalam tentang IT.

### 1.2 Tujuan Praktikum 

Untuk mengetahui cara menginstal Ubuntu berbasis Linux.

### 1.3 Bahan dan Alat Praktikum

- Komputer/laptop/PC  
- CD Linux

---

## BAB 2: PEMBAHASAN

### 2.1 Pengertian Sistem Operasi

Sistem operasi atau operating system adalah kumpulan program yang bertugas mengelola sumber daya perangkat keras komputer dan menyediakan layanan umum untuk aplikasi perangkat lunak. Sistem operasi merupakan jenis perangkat lunak sistem yang paling penting dalam sebuah komputer. Tanpa sistem operasi, pengguna tidak akan bisa menjalankan program aplikasi di komputer mereka, kecuali program booting. 

### 2.2 Pengertian Linux

Linux atau GNU/Linux adalah sistem operasi yang bebas dan sangat populer untuk digunakan pada komputer. Istilah ini sering merujuk pada keseluruhan distribusi Linux (Linux distribution), yang mencakup berbagai program pendukung sistem operasi. Linux merupakan contoh utama dari hasil pengembangan perangkat lunak yang bebas dan sumber terbuka. Seperti halnya perangkat lunak bebas dan sumber terbuka lainnya, kode sumber Linux dapat dimodifikasi, digunakan, dan didistribusikan kembali oleh siapa saja tanpa batasan.

### 2.3 Pengertian Ubuntu

Ubuntu adalah salah satu distribusi Linux yang berbasis pada Debian dan disebarkan sebagai perangkat lunak open source. Nama Ubuntu diambil dari sebuah filosofi Afrika Selatan yang berarti "kemanusiaan kepada sesama." Ubuntu dirancang untuk penggunaan pribadi, tetapi juga tersedia dalam versi server yang telah digunakan secara luas.

### 2.4 Langkah-langkah Instalasi Sistem Operasi Linux

1. Masukkan DVD Ubuntu 14.04 LTS installer (download di [http://releases.ubuntu.com/14.04/](http://releases.ubuntu.com/14.04/)) yang sudah di burn dalam DVD, sebelumnya atur di BIOS untuk pengaturan booting dengan DVD-ROOM sebagai primer pertama booting. Tunggu hingga proses booting sampai keluar tampilan.
2. Pilih bahasa instalasi dan bahasa sistem operasi kemudian pilih opsi **Install Ubuntu** untuk memulai proses instalasi.
3. Atur pengaturan jaringan jika diperlukan dan klik **Continue**.
4. Pilih jenis instalasi, biasanya Anda dapat memilih **Erase disk and install Linux Mint** jika ini adalah instalasi bersih. Jika Anda menginstal bersama sistem operasi lain, pilih opsi yang sesuai.
5. Masukkan informasi pengguna seperti nama Anda, nama komputer, nama pengguna, dan password. Klik **Continue**.
6. Tunggu hingga proses instalasi selesai. Proses ini memakan waktu beberapa menit. Setelah selesai, Anda akan diminta untuk me-restart mesin virtual.
7. Setelah restart, login ke Linux Mint menggunakan username dan password yang telah Anda buat.
8. Setelah semua proses instalasi selesai maka Anda sekarang dapat mulai menggunakan Linux Mint.

---

## BAB 3: ANALISA

1. **Buatlah laporan proses instalasi di komputer mahasiswa dan tampilkan screenshotnya.**  
   **Jawab:**  
   Gambar di atas menyatakan bahwa telah selesai menginstall Linux.

2. **Analisislah pada gambar kenapa saat instalasi perlu dipilih “/” pada opsi Mount Point?**  
   **Jawab:**  
   Karena partisi root ("/") merupakan hirarki tertinggi dari sistem direktori Linux di mana direktori ini membawahi direktori /usr, /home, /mnt, dan direktori lainnya. Ketika memilih "Mount Point" sebagai "/", artinya partisi tersebut akan digunakan sebagai root directory, yang merupakan titik awal dari seluruh sistem file pada Linux. Partisi ini mutlak harus ada di dalam sistem Linux seperti halnya Drive C: pada Windows. Sehingga jika saat pembagian partisi tidak ada root ("/") maka sistem Linux tidak bisa berjalan.

3. **Berikan penjelasan tentang ext4, ext3, swap, ntfs, fat32, btrfs!**

   **Jawab:**
   - **ext4**: Ext4 dirilis secara komplit dan stabil berawal dari kernel 2.6.28, jadi apabila distro Anda secara default memiliki versi kernel tersebut atau di atasnya, otomatis sistem Anda sudah support ext4 (dengan catatan sudah di-include ke dalam kernelnya). Selain itu, versi e2fsprogs harus menggunakan versi 1.41.5 atau lebih. Keuntungan yang bisa didapat dengan mengupgrade filesystem ke ext4 dibanding ext3 adalah mempunyai pengalamatan 48-bit block yang artinya dia akan mempunyai 1EB = 1,048,576 TB ukuran maksimum filesystem dengan 16 TB untuk maksimum file size-nya, fast fsck, journal checksumming, dan defragmentation support. 

   - **ext3**: EXT3 adalah peningkatan dari EXT2 file system. Ext3 merupakan suatu journalled file system. Journalled file system didesain untuk membantu melindungi data yang ada di dalamnya. Dengan adanya journalled file system, maka kita tidak perlu lagi melakukan pengecekan kekonsistensian data, yang akan memakan waktu sangat lama bagi harddisk yang berkapasitas besar.

   - **swap**: Swap digunakan sebagai Virtual Memory atau ibaratnya RAM cadangan jika RAM yang asli sudah tidak mumpuni untuk memproses aplikasi, partisi swap inilah yang menghandlenya. Akan tetapi yang perlu diingat adalah partisi swap hanya virtual memory saja, bukan RAM yang sesungguhnya atau File System yang digunakan sebagai tempat penyimpanan data, tetapi sebagai virtual memory, yaitu sebagai pembantu kinerja dari memory.

   - **ntfs**: NTFS (New Technology File System) adalah sebuah sistem berkas yang diperkenalkan oleh Microsoft dalam kumpulan sistem operasi Windows NT, yang terdiri dari Windows 2000, Windows XP, Windows Server 2003, Windows Vista, Windows 7.

   - **fat32**: Sistem file tertua yang dikembangkan pada tahun 1970-an yang tersedia untuk sistem operasi Windows. Ini pada dasarnya dirancang untuk floppy drive yang memiliki ukuran kurang dari 500 K. Ada tiga versi FAT - FAT12, FAT16, dan FAT32, dan mereka berbeda dalam ukuran file dan struktur pada disk.

   - **btrfs**: B-Tree File System (BTRFS, kadang singkatan ini juga diucapkan BuTteR FS atau BeTteR FS) merupakan sebuah file system di bawah lisensi General Public License (GPL). B-Tree File System ini membuat Linux dapat lebih “mengatur” storage atau tempat penyimpanan yang ada. "Mengatur" dalam hal ini bukan berarti hanya mengatur dalam hal pengalaman saja, namun juga dapat melakukan administrasi dan pengelolaan tempat penyimpanan tersebut dengan interface yang lebih bersih sehingga pengguna dapat melihat apa yang sedang dipakai dan dikerjakan, serta membuatnya menjadi lebih “terpercaya”.
