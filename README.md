# Capstone-Modul-2-Data-Analysis

**Deskripsi Proyek**

Proyek ini bertujuan untuk menganalisis permasalahan nyata yang dihadapi oleh layanan TransJakarta berdasarkan data transaksi penumpang, dan bagaimana rekomendasi perbaikannya secara bisnis.
Berdasarkan analisis data dan dukungan informasi dari sumber eksternal, berikut adalah enam permasalahan utama yang menjadi fokus proyek ini:
1. Kepadatan Penumpang dan Keterlambatan Bus
2. Penyerobotan Jalur Busway oleh Kendaraan Pribadi
3. Perubahan Rute dan Kekhawatiran Penumpang
4. Perubahan Nama Halte yang Membingungkan Penumpang
5. Pelanggaran Tap Out dan Pemotongan Saldo Ganda
6. Kartu Elektronik Digunakan oleh Banyak Orang
Melalui analisis yang berfokus pada enam isu ini, diharapkan ditemukan insight yang dapat menjadi dasar rekomendasi peningkatan kualitas layanan TransJakarta dari sisi operasional dan pengalaman pelanggan.

**Dataset**

Dataset transaksi TransJakarta terdiri dari 37.900 baris dan 22 kolom, yang merekam aktivitas perjalanan penumpang menggunakan sistem tap-in dan tap-out. Data ini mencakup informasi pengguna, lokasi halte, waktu perjalanan, dan pembayaran.

**Teknik analisis**

Statistik deskriptif dan statistik inferensial yang menggunakan t-test dan chi-square. 

**Kesimpulan dan saran**

Berdasarkan hasil analisis data Transjakarta, dapat disimpulkan bahwa:

1. Kondisi Layanan Transjakarta
   - Waktu tempuh perjalanan pada jam sibuk (06.00–09.00 & 16.00–19.00) rata-rata mencapai 74,5 menit, jauh lebih lama dibanding jam non-sibuk.
   - Koridor “Kampung Rambutan - Blok M” memiliki durasi perjalanan rata-rata tertinggi (~85 menit) dan berada dalam daftar 10 koridor dengan volume penumpang terendah — indikasi adanya hambatan atau kurangnya efisiensi.
   - Halte Penjaringan menjadi titik masuk penumpang terbanyak, diikuti oleh halte Garuda Taman Mini dan BKN.
   - Jumlah penumpang sangat terkonsentrasi pada hari kerja (±6.800 per hari), dibandingkan akhir pekan (~1.800 per hari).

2. Pola Penggunaan dan Masalah Operasional
   - Sebanyak 1.344 transaksi (3.55%) tidak memiliki data tap-out, dan 709 di antaranya tetap dikenakan biaya, menunjukkan potensi masalah sistem atau kepatuhan pengguna.
   - Ditemukan 4 kasus transaksi duplikat (waktu & halte tap-in sama), yang dapat menimbulkan error pada pencatatan jumlah penumpang.
   - Tidak ditemukan indikasi penyalahgunaan kartu elektronik berdasarkan perbedaan gender atau tahun lahir, maupun penggunaan kartu dalam waktu yang terlalu singkat.

3. Distribusi & Utilisasi Koridor
   - Beberapa koridor seperti “Rusun Marunda – Waduk Pluit” memiliki interquartile range durasi perjalanan yang tinggi (~58 menit), menunjukkan inkonsistensi waktu tempuh.
   - Terdapat 10 koridor dan 10 halte yang hanya mencatat ≤54 transaksi, bahkan beberapa halte hanya tercatat 1 transaksi — perlu evaluasi apakah masih aktif, terimbas proyek konstruksi, atau tidak strategis.

4. Kualitas Data
   - Tidak ditemukan inkonsistensi dalam penamaan halte atau koordinat GPS. Artinya, sistem sudah cukup konsisten dalam pencatatan lokasi dan identitas halte.

**Rekomendasi**

Cara meningkatkan jumlah pelanggan Transjakarta dan meningkatkan kepuasan pelanggan saat menggunakan layanan Transjakarta:

1. Penambahan petugas halte terutama di halte ramai pelanggan dan di jam sibuk agar dapat mengatur penumpang.
2. Penambahan bus untuk rute dengan jumlah pelanggan terbanyak dan mempersempit headway bus dan juga memperbanyak frekuensi bus terutama pada jam-jam sibuk agar waktu tunggu bus tidak terlalu lama.  
3. Untuk meningkatkan efisiensi waktu perjalanan, Transjakarta dapat mempertimbangkan rekomendasi berikut:
   * Evaluasi dan sesuaikan rute bus untuk meminimalkan kemungkinan macet atau jalan yang lambat.
   * Tingkatkan frekuensi layanan bus pada rute yang sering mengalami kemacetan untuk mengurangi waktu tunggu penumpang.
   * Perbarui sistem informasi penumpang untuk memberikan estimasi waktu perjalanan yang lebih akurat dan informasi terkini mengenai kondisi lalu lintas melalui aplikasi yang informasinya bisa diakses secara realtime oleh penumpang.
4. Dengan jumlah pelanggan yang didominasi oleh perempuan dan didominasi oleh orang dewasa maka perlu adanya penambahan bus dan ruang khusus perempuan di setiap bus layanan Transjakarta. Saat ini, Transjakarta memiliki bus pink yang hanya ada di beberapa koridor tertentu saja yaitu koridor 2, koridor 3, koridor 9, koridor 13 dan koridor 5. Maka bisa dilakukan penambahan di semua koridor dan layanan khususnya di koridor ramai pelanggan. 
5. Mayoritas metode pembayaran pelanggan adalah bank DKI, hal ini menunjukkan bahwa mayoritas pelanggan Transjakarta adalah pengguna bank DKI. Di halte Transjakarta ada vending machine yang menjual kartu. Transjakarta harus menyediakan kartu bank DKI lebih banyak dibandingkan dengan jenis kartu lainnya atau lebih mempromosikan metode pembayaran lainnya kepada pelanggan. 
6. Layanan yang sering digunakan oleh pelanggan adalah layanan reguler, layanan reguler juga harus disediakan armada yang banyak karena minatnya banyak dibandingkan layanan lainnya agar waktu tunggu penumpang tidak lama dan load factor bus tidak melebihi kapasitas.
7. Dari visualisasi origin-destination di Tableau pun bahwa Layanan Transjakarta sudah mencakup seluruh wilayah DKI Jakarta, maka perlu adanya peningkatan promosi mengenai layanan dan peningkatan layanan untuk menarik minat masyarakat untuk menggunakan layananan Transjakarta.
