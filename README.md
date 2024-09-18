# Jarkom-Modul-1-IT27-2024

## IT 27

| No  | Nama Anggota          | NRP        |
| --- | --------------------- | ---------- |
| 1   | Danendra Fidel Khansa | 5027231063 |
| 2   | Farida Qurrotu A'yuna | 5027231015 |

### Pegawai Negeri Sebelah

  Langkah Penyelesaian:

  1. Gunakan filter TCP pada Wireshark untuk mencari file pns.csv.
  2. Setelah file ditemukan, lakukan filter 
  3. Lanjut pada paket-paket yang berkaitan.
  4. Flag ditemukan

### Illegal Breakthrough

  Langkah Penyelesaian:

  1. Filter http.response pada Wireshark.
  2. Cari paket dengan IP belakang 207.
  3. Lakukan pencarian lebih lanjut pada paket yang mengandung kata kunci "found".
  4. Jawaban soal dan tools yang digunakan, yaitu ffuf-v2.1.0-dev, ditemukan di dalam paket yang berkaitan.
  5. Flag ditemukan

### Rizzset

  Langkah Penyelesaian :

  1. Filter paket DNS pada Wireshark, kemudian temukan IP terkait di bagian pojok kanan bawah.
  2. Clone repository JARM dengan perintah berikut:
  ```py
  git clone https://github.com/armory/jarm.git
  cd jarm
  pip install -r requirements.txt
  ```
  3. Jalankan perintah berikut untuk melakukan JARM fingerprinting terhadap domain target:
  ```py
  python jarm.py www.its.ac.id
  ```
  4. Hasil fingerprint ditemukan
  5. Muncul Flag

### Stegography

   Langkah Penyelesaian :

   1. Gunakan filter frame contains "png" pada Wireshark.
   2. Ekspor objek dan simpan gambar terkait.
   3. Gunakan script reversed.py yang sudah dimodifikasi untuk mendekripsi pesan di dalam gambar.
   4. Dari gambar ATP, EH, dan KJK, hasil yang ditemukan adalah frasa "pahlawan keamanan siber."
   5. Flag ditemukan

### InneRCE

  Langkah Penyelesaian :

  1. Filter frame contains "shel" untuk mencari file yang berhubungan dengan webshell.
  2. Fokus pada timestamp 2024-09-16 13:18:05.
  3. Cari hostname pada pojok kanan untuk file upload.php_server-app dan upload webshell dengan nama idzoyyshell.php.
  4. Jalankan command whoami sebagai command pertama.
  5. Cari paket yang berisi echo dan decode string berikut:
```
cGxzIHJhdGUgc29hbCBpbmkK
```
  6. Hasil decoding: "pls rate soal ini".
  7. Flag ditemukan

### Gajah Terbang (Server Record)

  Langkah Penyelesaian:
  1. Gunakan filter tcp.port == 5432 untuk PostgreSQL dan tcp.port == 6969 untuk mengecek port lain.
  2. Temukan Debian pada salah satu file melalui filter tcp.options -> tcp.stream eq 9.
  3. Pada file yang sama, di pojok kiri atas, temukan credentials untuk user s1gm4 dan nama database sigmaskibidigyatrizzzz.
  4. Lakukan penghitungan manual jumlah pengguna dalam database, ditemukan ada 4 pengguna.
  5. Temukan email admin jojohermawan@gmail.com, dan dekripsi hash password yang menghasilkan admin1234.
  6. Flag ditemukan

