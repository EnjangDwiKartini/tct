## Cara Membangun SaaS
![alt text](https://github.com/EnjangDwiKartini/tct/blob/master/images/SaaS-1.jpg "Saas")
***
**SaaS (software as a service atau perangkat lunak berbentuk layanan)** adalah suatu model penyampaian aplikasi perangkat lunak
 oleh suatu vendor perangkat lunak yang mengembangkan aplikasi web yang diinangi dan dioperasikan (baik secara mandiri maupun melalui
 pihak ketiga) untuk digunakan oleh pelanggannya melalui Internet. 

 ---

**Karakteristik Software-as–a-Service (SaaS)**
- Membuat dan mengakses aplikasi SaaS melalui internet
- Aplikasi software diurus oleh vendor bukan pelanggan
- Lisensi untuk penggunaan aplikasi bersifat subscription (perbulan/pertahun), dan ditagih setiap bulan atau tahun.
- Aplikasi SaaS hemat biaya karena tidak memerlukan maintenance oleh pelanggan.
- Aplikasi tersedia sesuai permintaan
- Aplikasi dapat di upgrade sesuai permintaan
- SaaS menawarkan model sharing data. 
- Semua pengguna menjalankan versi software yang sama.

---

**Kelebihan Software-as–a-Service (SaaS)**
- Software aplikasi yang sederhana namun bermanfaat 
- Efisien penggunaan lisensi software 
- Pelanggan dapat memiliki lisensi tunggal untuk beberapa komputer yang berjalan di lokasi yang berbeda yang mengurangi biaya lisensi
- Pengelolaan dan data terpusat 
- Cloud computing  menyimpan data secara terpusat. Namun, penyedia cloud dapat menyimpan data dengan cara yang terdesentralisasi demi redundansi dan reliabilitas
- Tanggung jawab platform dikelola oleh vendor SaaS 
- Semua tanggung jawab platform seperti backup, pemeliharaan sistem, keamanan, penyegaran perangkat keras, manajemen daya, dll dilakukan oleh penyedia cloud

---

**Kekurangan Software-as–a-Service (SaaS)**
- Rentan terkena virus internet 
- Jika pelanggan mengunjungi situs web dan browser berbahaya yang terinfeksi virus, akses selanjutnya ke aplikasi SaaS mungkin akan membahayakan data pelanggan
- Ketergantungan dengan internet 
- Aplikasi SaaS hanya bisa berjalan bila jaringan internet tersedia
- Tidak bisa berbagi beban kerja cloud 
- Mentransfer beban kerja dari satu cloud SaaS ke cloud SaaS lainya tidak mudah karena alur kerja, logika bisnis, antarmuka pengguna, skrip dukungan dapat menjadi penyedia spesifik.

---

**Bagaimana Cara Membangun SaaS ?????**

SaaS pada umumnya menggunakan antarmuka web dan menggunakan Javascript disisi Client. 
Berikut hal yang perlu dipersiapkan untuk membangun SaaS:
- Bangun API 
- Scalable Database 
- Manajemen Pengguna (Daftar, Login dengan verifikasi Email dan SMS)
- Situs web HTTP (S3 + Cloudfront / Netlify + AWS Certificate Manager)
	* S3 : Layanan penyimpanan data yang dapat Anda gunakan untuk melayani halaman HTML untuk situs web sederhana.
	* Cloudfront :  Jaringan Pengiriman Konten, itu cache halaman situs sehingga pengguna selanjutnya dapat mengakses situs kita lebih cepat tanpa harus membaca dari S3. 
![alt text](https://github.com/EnjangDwiKartini/tct/blob/master/images/SaaS-2.png "SaaS")

Secara umum struktur dari SaaS adalah sebagai berikut :
* Aplikasi yang dihosting 
* Alat pengembangan, manajemen basis data, analisis bisnis 
* Sistem Operasi 
* Server dan Penyimpanan 
* Jaringan firewall / Keamanan 
* Pusat Data