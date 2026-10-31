# Test Case Generator

Aplikasi web ringan dan responsif untuk menyusun draf kasus pengujian perangkat lunak berdasarkan kebutuhan fitur. Test Case Generator membantu QA Engineer, Pengembang Perangkat Lunak, dan anggota tim produk lainnya mengubah deskripsi fitur menjadi kumpulan awal skenario pengujian yang terstruktur, meliputi skenario positif, negatif, validasi, dan batas nilai.

> **Status proyek:** Prototipe sisi front-end. Saat ini, pembuatan kasus pengujian menggunakan aturan dan templat JavaScript yang telah ditentukan. Aplikasi belum memanggil LLM, layanan AI eksternal, maupun API back-end.

## Daftar Isi

- Gambaran Umum Proyek
- Permasalahan
- Tujuan
- Pengguna Sasaran
- Fitur Utama
- Cara Kerja
- Kategori Kasus Pengujian
- Teknologi yang Digunakan
- Struktur Proyek
- Persiapan dan Menjalankan Aplikasi
- Cara Penggunaan
- Hasil yang Dihasilkan
- Keterbatasan
- Potensi Pengembangan Selanjutnya
- Kontribusi
- Lisensi

## Gambaran Umum Proyek

Test Case Generator merupakan alat berbasis peramban yang dirancang untuk menyederhanakan tahap awal penyusunan kasus pengujian perangkat lunak. Pengguna memasukkan nama fitur, deskripsi kebutuhan, dan skenario utama (opsional). Selanjutnya, aplikasi menghasilkan draf kasus pengujian yang terstruktur dan menampilkan hasilnya dalam bentuk tabel.

Antarmuka aplikasi menggunakan tampilan yang bersih dengan tema warna krem dan biru, serta tata letak responsif untuk layar desktop maupun perangkat seluler. Kasus pengujian yang dihasilkan dapat disalin atau diekspor ke dalam berkas CSV sehingga draf lebih mudah ditinjau, disunting, dan digunakan dalam alur kerja QA.

Aplikasi ini ditujukan untuk membantu proses analisis pengujian, bukan menggantikan analisis profesional. Setiap skenario yang dihasilkan perlu ditinjau berdasarkan kebutuhan produk dan perilaku aplikasi yang sebenarnya sebelum digunakan dalam siklus pengujian resmi.

## Permasalahan

Penyusunan kasus pengujian secara manual dapat membutuhkan waktu yang cukup lama. Seorang QA Engineer perlu memahami kebutuhan, mengidentifikasi kondisi pengujian, menyiapkan data masukan, menentukan langkah pelaksanaan, dan menetapkan hasil yang diharapkan. Ketika kebutuhan sering berubah atau tim menangani banyak fitur, pekerjaan tersebut dapat menjadi berulang dan sulit distandardisasi.

Penyusunan secara manual juga dapat menyebabkan dokumentasi yang tidak konsisten atau cakupan skenario yang kurang lengkap. Tim mungkin terlalu berfokus pada alur keberhasilan yang diharapkan, sementara masukan tidak valid, pemeriksaan kolom wajib, dan kondisi batas nilai justru terlewatkan. Kekurangan tersebut dapat mengurangi efektivitas pengujian dan menyebabkan cacat perangkat lunak tidak terdeteksi hingga tahap berikutnya.

Test Case Generator membantu mengatasi tantangan alur kerja tersebut dengan menyediakan cara cepat untuk membuat kumpulan awal skenario pengujian yang memiliki struktur konsisten berdasarkan informasi fitur yang diberikan pengguna.

## Tujuan

- Mengurangi upaya yang diperlukan untuk menyusun draf skenario pengujian umum.
- Menyediakan struktur yang konsisten untuk dokumentasi kasus pengujian.
- Mendorong pemeriksaan skenario positif, negatif, validasi, dan batas nilai.
- Memudahkan pengguna meninjau, menyalin, dan mengekspor hasil yang dihasilkan.
- Menyediakan prototipe ringan yang dapat dijalankan langsung melalui peramban web modern.

## Pengguna Sasaran

| Pengguna | Manfaat aplikasi |
| --- | --- |
| QA Engineer / Analis Pengujian | Menyiapkan draf awal kasus pengujian dan meninjau cakupan skenario. |
| QA Lead / Test Lead | Menggunakan format awal yang konsisten saat meninjau dokumentasi pengujian. |
| Pengembang Perangkat Lunak | Mengidentifikasi skenario dasar yang perlu dipertimbangkan saat mengimplementasikan atau melakukan debugging fitur. |
| Product Manager / Analis Bisnis | Meninjau bagaimana kebutuhan fitur dapat diterjemahkan menjadi skenario yang dapat diverifikasi. |

## Fitur Utama

### 1. Masukan kebutuhan

Pengguna dapat memasukkan:

- **Nama fitur** — nama fitur yang akan diuji.
- **Deskripsi kebutuhan** — penjelasan singkat mengenai aturan dan perilaku yang diharapkan dari fitur.
- **Skenario utama** — deskripsi opsional mengenai alur utama yang berhasil.

### 2. Pemilihan kategori pengujian

Pengguna dapat memilih satu atau beberapa kategori berikut:

- Positif
- Negatif
- Validasi
- Batas nilai (*Boundary*)

### 3. Pembuatan kasus pengujian

Aplikasi menerapkan templat JavaScript yang telah ditentukan dan pemeriksaan kebutuhan yang dipilih untuk menghasilkan draf skenario. Hasilnya mencakup:

- ID Kasus Pengujian
- Jenis Pengujian
- Skenario
- Langkah Pengujian
- Hasil yang Diharapkan

### 4. Menyalin hasil

Tindakan **Salin Semua** menyalin data tabel yang dihasilkan ke papan klip dalam bentuk teks yang kompatibel dengan CSV, apabila akses papan klip tersedia di peramban.

### 5. Ekspor CSV

Tindakan **Unduh CSV** mengekspor kasus pengujian yang dihasilkan ke dalam berkas `test-cases.csv`, yang dapat dibuka menggunakan aplikasi pengolah spreadsheet.

### 6. Antarmuka responsif

Tata letak menyesuaikan ukuran layar yang lebih kecil sehingga formulir masukan dan hasil tetap dapat digunakan pada perangkat seluler.

### 7. Validasi masukan dan pengaturan ulang

Aplikasi memeriksa kolom wajib dan mengharuskan pengguna memilih setidaknya satu kategori pengujian. Pengguna juga dapat memuat contoh masukan, mengatur ulang formulir, dan menghasilkan kumpulan kasus pengujian baru.

## Cara Kerja

1. Pengguna memasukkan nama fitur dan deskripsi kebutuhan.
2. Pengguna dapat menambahkan skenario utama secara opsional.
3. Pengguna memilih satu atau beberapa kategori pengujian.
4. Pengguna mengeklik **Buat Kasus Pengujian**.
5. JavaScript memvalidasi formulir dan memilih templat yang telah ditentukan serta sesuai dengan masukan.
6. Draf hasil pembuatan ditampilkan pada tabel hasil.
7. Pengguna meninjau hasilnya, kemudian dapat menyalin atau mengunduh data tersebut.

### Pendekatan pembuatan

Implementasi saat ini menggunakan pendekatan **berbasis aturan dan templat** (*rule-based and template-driven*). Sebagai contoh, aplikasi menambahkan skenario validasi dasar ketika deskripsi kebutuhan menyebutkan alamat email. Aplikasi juga dapat mengenali frasa batas minimum numerik, seperti `minimum 8 karakter`.

Pendekatan ini merupakan heuristik sederhana, bukan kemampuan penalaran bahasa alami. Aplikasi mungkin tidak memahami semua variasi penulisan kebutuhan dan tidak menjamin cakupan pengujian yang lengkap.

## Kategori Kasus Pengujian

| Kategori | Tujuan | Contoh skenario |
| --- | --- | --- |
| Positif | Memastikan alur yang valid dan diharapkan dapat berjalan. | Mengirimkan kredensial masuk yang valid. |
| Negatif | Memastikan kondisi yang tidak valid atau tidak dapat diterima ditolak. | Mengirimkan kredensial yang salah atau data dengan format tidak sesuai. |
| Validasi | Memeriksa kolom wajib dan aturan format masukan. | Mengirimkan formulir dengan kolom wajib yang masih kosong. |
| Batas nilai (*Boundary*) | Memeriksa nilai pada atau di sekitar batas yang ditentukan. | Menguji nilai tepat di bawah dan tepat pada panjang minimum. |

Skenario yang dihasilkan bergantung pada teks kebutuhan dan templat yang saat ini diterapkan di `script.js`. Pengguna perlu menambahkan atau menyesuaikan kasus apabila fitur memiliki aturan bisnis tambahan.

## Teknologi yang Digunakan

| Teknologi | Penggunaan |
| --- | --- |
| HTML5 | Struktur halaman, kontrol formulir, dan tabel hasil. |
| CSS3 | Desain visual, tata letak, perilaku responsif, dan tampilan interaksi. |
| JavaScript Murni (*Vanilla JavaScript*) | Validasi formulir, pembuatan kasus berbasis aturan, penampilan tabel, penyalinan ke papan klip, dan ekspor CSV. |
| API Peramban | Fungsionalitas papan klip serta Blob/URL objek untuk mengekspor data. |

Prototipe saat ini tidak memerlukan framework, pengelola paket, basis data, server, maupun alat *build*.

## Struktur Proyek

```text
Test-Case-Generator-Redesigned/
├── index.html      # Struktur aplikasi dan formulir masukan
├── style.css       # Pengaturan tampilan responsif dan desain visual
├── script.js       # Logika validasi, pembuatan, penampilan, dan ekspor
└── README.md       # Dokumentasi proyek
```

## Persiapan dan Menjalankan Aplikasi

### Persyaratan

- Peramban web modern (Chrome, Edge, Firefox, atau Safari).
- Tidak perlu memasang Node.js maupun paket pihak ketiga.

### Menjalankan secara lokal

1. Unduh atau klon repositori ini.
2. Ekstrak berkas proyek apabila tersedia dalam arsip ZIP.
3. Buka folder `Test-Case-Generator-Redesigned`.
4. Buka berkas `index.html` melalui peramban.

Sebagai alternatif, jalankan server lokal sederhana dari direktori proyek:

```bash
python3 -m http.server 8000
```

Kemudian buka alamat berikut:

```text
http://localhost:8000
```

## Cara Penggunaan

1. Masukkan **Nama Fitur**.
2. Masukkan **Deskripsi Kebutuhan**.
3. Masukkan **Skenario Utama** jika diperlukan.
4. Pilih kategori kasus pengujian yang ingin dibuat.
5. Klik **Buat Kasus Pengujian**.
6. Tinjau ID, skenario, langkah pengujian, dan hasil yang diharapkan.
7. Klik **Salin Semua** untuk menyalin hasil atau **Unduh CSV** untuk mengekspornya.
8. Sunting draf sesuai kebutuhan agar mencerminkan spesifikasi produk secara lengkap.

### Contoh masukan

**Nama fitur**

```text
User Login
```

**Deskripsi kebutuhan**

```text
Pengguna dapat masuk menggunakan alamat email dan kata sandi yang telah terdaftar.
Email harus menggunakan format yang valid dan kata sandi harus terdiri dari
minimal 8 karakter.
```

**Skenario utama**

```text
Masukkan email yang telah terdaftar dan kata sandi yang benar, kemudian pilih Masuk.
```

**Kategori yang dipilih:** Positif, Negatif, Validasi, dan Batas Nilai.

Aplikasi membuat draf skenario berdasarkan templat yang telah diimplementasikan dan pemeriksaan kebutuhan sederhana. Hasil yang tepat dapat berubah seiring perkembangan kode sumber.

## Hasil yang Dihasilkan

Tabel hasil menggunakan kolom berikut:

| Kolom | Deskripsi |
| --- | --- |
| ID | Identitas kasus pengujian yang dibuat, misalnya `TC-001`. |
| Jenis | Kategori pengujian. |
| Skenario | Kondisi atau perilaku yang perlu diverifikasi. |
| Langkah Pengujian | Tindakan tingkat tinggi yang perlu dilakukan. |
| Hasil yang Diharapkan | Perilaku yang diharapkan untuk dibandingkan dengan hasil aktual. |

Berkas CSV dapat digunakan sebagai bahan awal untuk peninjauan melalui aplikasi spreadsheet. Berkas tersebut belum terintegrasi secara langsung dengan Jira, TestRail, atau platform manajemen pengujian lainnya.

## Keterbatasan

- Pembuatan kasus menggunakan aturan JavaScript lokal dan templat yang telah ditentukan; aplikasi belum didukung oleh model AI generatif.
- Belum tersedia back-end, basis data, autentikasi, maupun sinkronisasi cloud.
- Kasus pengujian yang dihasilkan merupakan saran awal dan mungkin memerlukan peninjauan atau penyuntingan yang cukup besar.
- Interpretasi kebutuhan terbatas pada pola yang secara eksplisit ditangani di `script.js`.
- Prototipe saat ini tidak menjalankan pengujian terhadap aplikasi secara langsung.
- Aplikasi belum menghasilkan skrip otomatisasi pengujian Selenium, Cypress, atau Playwright.
- Ekspor CSV tersedia, tetapi sinkronisasi langsung dengan Jira atau TestRail belum diimplementasikan.

## Potensi Pengembangan Selanjutnya

Beberapa pengembangan yang dapat dipertimbangkan untuk versi berikutnya meliputi:

1. **Integrasi LLM** — menghubungkan API model bahasa untuk menafsirkan kebutuhan secara lebih kontekstual dan mengusulkan skenario yang lebih kaya.
2. **Arsitektur prompt dan mekanisme pengaman** — menggunakan prompt berlapis, batasan eksplisit, skema keluaran terstruktur, dan pembuatan skenario yang berlandaskan kebutuhan.
3. **Ekspor Gherkin / BDD** — menghasilkan skenario Given-When-Then untuk *behavior-driven development*.
4. **Pembuatan skrip pengujian otomatis** — membuat skrip awal Selenium, Cypress, atau Playwright yang dapat ditinjau.
5. **Integrasi manajemen pengujian** — menyinkronkan kasus pengujian yang telah disetujui dengan Jira atau TestRail.
6. **Integrasi CI/CD** — mendukung alur kerja menggunakan GitHub Actions atau GitLab CI.
7. **Penyimpanan dan kolaborasi** — menambahkan akun pengguna, ruang kerja proyek, penyimpanan basis data, dan riwayat kasus pengujian.
8. **Alur validasi** — menambahkan tahap peninjauan terpisah untuk menandai kebutuhan yang ambigu, duplikasi, dan asumsi yang tidak didukung.

## Kontribusi

Kontribusi dan saran sangat terbuka. Kontribusi yang bermanfaat sebaiknya:

- Menjelaskan masalah atau peningkatan yang diusulkan.
- Mempertahankan kemudahan penggunaan aplikasi tanpa menambahkan dependensi yang tidak diperlukan, kecuali jika memang beralasan.
- Menyertakan langkah pengujian yang jelas untuk setiap perubahan perilaku.
- Memperbarui README apabila fitur atau keterbatasan aplikasi berubah.

## Lisensi

Proyek ini belum memiliki lisensi yang ditentukan. Tambahkan berkas `LICENSE` sebelum mendistribusikan ulang atau menggunakan kembali proyek ini dengan lisensi sumber terbuka.
