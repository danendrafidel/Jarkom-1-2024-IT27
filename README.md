# Jarkom-Modul-1-IT27-2024

## IT 27

| No  | Nama Anggota          | NRP        |
| --- | --------------------- | ---------- |
| 1   | Danendra Fidel Khansa | 5027231063 |
| 2   | Farida Qurrotu A'yuna | 5027231015 |

## Advancing Sanity

  ### Langkah Penyelesaian : 

  1. Filter dengan http contains “username” untuk menemukan usernamenya yaitu **JaneD03**
  ![Cuplikan layar 2024-09-20 191847](https://github.com/user-attachments/assets/1b9abdfd-fab4-4ca4-b4a9-d5ebdf538242)

  2. Filter dengan http containts “.txt”. lalu ditemukan file Clue3.txt
  ![Cuplikan layar 2024-09-20 192042](https://github.com/user-attachments/assets/68fe0ee3-69d0-4679-8108-932df79db5d9)

  3. Pada Clue3.txt dibawah kata tersebut kita diarahkan untuk membuka PPT peraturan soal shift jarkom
  4. Saat melihat Peraturan Soal Shift pada PPT terdapat sesuatu kode yang harus kita decode menggunakan base64.
  5. Input hasil Decodenya

  ![Cuplikan layar 2024-09-19 021936](https://github.com/user-attachments/assets/c5746a9f-31ea-497e-b4fe-a4e1729976ea)
  ![Cuplikan layar 2024-09-19 010931](https://github.com/user-attachments/assets/cc5dd92d-c9b7-4b50-9738-fe4725f3fef9)
  
  7. Flag muncul
  ![Cuplikan layar 2024-09-20 192159](https://github.com/user-attachments/assets/81012aef-cbe4-4b61-8ba8-efe256692725)

## Pegawai Negeri Sebelah

  ### Langkah Penyelesaian:

  1. Gunakan filter TCP pada Wireshark untuk mencari info STOR data_pns.csv setelah itu lakukan find and select.
  ![Cuplikan layar 2024-09-20 193032](https://github.com/user-attachments/assets/fc4881e5-74dc-4ced-8322-cd8923be6c4e)
  ![Cuplikan layar 2024-09-20 193057](https://github.com/user-attachments/assets/d78db605-e491-4175-a33c-d0180182bf32)

  2. Setelah file ditemukan, lakukan filter dengan keyword "password"
  ![image](https://github.com/user-attachments/assets/2b7ce85f-a6d6-4e96-9a3a-02105df6465d)
  
  3. Lanjut pada paket-paket yang berkaitan.
  ![image](https://github.com/user-attachments/assets/d93b4b6a-3f57-497a-98e6-aee098f5f7be)
  
  4. Flag ditemukan
  ![Screenshot (145)](https://github.com/user-attachments/assets/70769ff5-c9a7-4dc1-bda2-7b92d9b654ef)

## Illegal Breakthrough

  #### Langkah Penyelesaian:

  1. Filter http.response pada Wireshark, kemudian cari yang ip belakangnya 207, ditemukan 172.21.88.207
  ![Cuplikan layar 2024-09-20 193729](https://github.com/user-attachments/assets/322bf522-d562-4f30-b1cf-20dc8f20cd7b)
  ![Cuplikan layar 2024-09-20 193800](https://github.com/user-attachments/assets/c79e9a41-879a-4a8a-9b30-96763b5e7071)

  2. Pada http.response tersebut cari info yang found bukan not found dan follow httpnya lalu ditemukan port 1917
  3. Endpoint berada disebelah post 
  4. Jawaban soal tools yang digunakan Fuzz Faster U Fool v2.1.0-dev, namun perlu dicari singkatan dari tools tersebut menjadi ffuf-v2.1.0-dev
  ![Cuplikan layar 2024-09-20 193822](https://github.com/user-attachments/assets/5c26f32a-d6ef-4bc0-bc28-58605eabe852)

  5. Flag ditemukan
  ![Cuplikan layar 2024-09-20 193641](https://github.com/user-attachments/assets/eea82829-a2a2-4a6f-a6ba-c9c6f1ee71d8)
![Cuplikan layar 2024-09-20 193630](https://github.com/user-attachments/assets/b519711e-1ce2-487f-a714-9bb8b375e895)

     
## Rizzset

  ### Langkah Penyelesaian :

  1. Filter dan ketikkan dns setelah tu display filter lg menggunakan CTRL + F kemudian ditemukan domain www.its.ac.id
  ![Cuplikan layar 2024-09-20 194917](https://github.com/user-attachments/assets/5fe99b02-dbfd-48ed-accb-982ca4bfb5ce)

  2. Setelah itu cari ip nya berbeda dari yang lain yaitu 103.94.189.5
  ![Cuplikan layar 2024-09-20 195142](https://github.com/user-attachments/assets/67968e07-baba-4365-aff7-5f5722363fba)

  3. Clone repository JARM dengan perintah berikut:
  ```py
  git clone https://github.com/armory/jarm.git
  cd jarm
  pip install -r requirements.txt
  ```
  4. Jalankan perintah berikut untuk melakukan JARM fingerprinting terhadap domain target:
  ```py
  python jarm.py www.its.ac.id
  ```
  5. Hasil fingerprint ditemukan
  ![Cuplikan layar 2024-09-19 000852](https://github.com/user-attachments/assets/1bb4dd8d-47ef-4e1c-a379-5180e864788f)

  6. Muncul Flag
  ![Cuplikan layar 2024-09-20 194643](https://github.com/user-attachments/assets/b0580544-d31b-4dc8-af69-f0268fc87f31)


## Stegography

   ## Langkah Penyelesaian :

  1. Download file pcap kemudian ekstrak
  ![Cuplikan layar 2024-09-20 195729](https://github.com/user-attachments/assets/c14540db-4973-4906-9d3d-ed19b68cbdcd)

  2. Lalu filter dengan frame contains "png", lalu export object -> pilih FTP DATA -> lalu save all, hitung gambarnya dan berjumlah 13
  ![Cuplikan layar 2024-09-20 195950](https://github.com/user-attachments/assets/c91cb1b7-2935-42f6-bc02-54046983f466)
  ![Cuplikan layar 2024-09-20 200031](https://github.com/user-attachments/assets/de5a2403-b48c-4aa4-86f7-95c113281012)
  ![Cuplikan layar 2024-09-20 200009](https://github.com/user-attachments/assets/b11a2872-3314-4ff7-a718-cbda7c52ce57)

  3. Lalu untuk mengurutkan gambarnya dengan merubah script reversed.py nya
  ```py
  from PIL import Image

def decode_image_reversed(image_path):
    img = Image.open(image_path)
    img = img.convert("RGB")
    pixels = img.load()

    binary_message = ""
    for i in range(img.width):
        for j in range(img.height):
            r, g, b = pixels[i, j]
            
            r_bin = format(r, '08b')
            binary_message += r_bin[-1]

    message = ""
    for i in range(0, len(binary_message), 8):
        byte = binary_message[i:i + 8]
        char = chr(int(byte, 2))
        
        if message.endswith("EOF"):
            break
        message += char

    message = message.replace("EOF", "")

    reversed_message = message[::-1]
    return reversed_message

# List image file
image_files = [
    "AI.png", "ATP.png", "EH.png", "IMK.png", "IOT.png", "KJK.png",
    "KWA.png", "SBD.png", "SISOP.png", "SOC.png", "SOKA.png",
    "TKA.png", "TKTI.png"
]

# Decode dan print pesan dari image
for image_file in image_files:
    decoded_message_reversed = decode_image_reversed(image_file)
    print(f"Pesan terbalik dari {image_file}: {decoded_message_reversed}")
```
  4. lalu run script py nya pake "python3 reversed.py" setelah itu akan muncul tulisan terbalik pada gambarnya yaitu pada gambar ATP, EH, KJK
  ```py
  python3 reversed.py
  ```
![Cuplikan layar 2024-09-20 200710](https://github.com/user-attachments/assets/1d353aeb-9814-466b-976c-5867881739e7)

  5. Lalu baca secara terbalik untuk mendapatkan flagnya dan hasilnya "pahlawan keamanan siber"

### InneRCE

  Langkah Penyelesaian :

  1. Filter frame contains "shel" untuk mencari file yang berhubungan dengan webshell, pada urutan no 98 akan menemukan webshellnya dan untuk melihat waktu upload hacker dilihat pada bagian bawah untuk jam uploadnya
  ![Cuplikan layar 2024-09-20 201232](https://github.com/user-attachments/assets/194feee5-c30e-4372-943b-9fab71601756)

  2. Kemudian frame contains "shell" untuk mencari endpointnya kemudian follow dan ditemukan "/upload.php" lalu mencari hostname dengan filter frame contains "hostname" follow setelah itu dibagian bawah terdapat hostnamenya yaitu server-app lalu gabung menjadi /upload.php_server-app
  ![Cuplikan layar 2024-09-20 201350](https://github.com/user-attachments/assets/7c18709c-1d03-4b2e-a448-e60597223faa)
  ![Cuplikan layar 2024-09-20 201320](https://github.com/user-attachments/assets/1a61e382-f439-424f-8d82-4f4b6ff52d95)

  3. Kembali lagi ke frame contains "shell" lalu lihat bagian info get untuk nama webshellnya yaitu idzoyyshell.php
  ![Cuplikan layar 2024-09-20 201706](https://github.com/user-attachments/assets/d019fa39-c25b-45f6-aa62-ed7e5798cf89)

  5. Lalu untuk command pertama cek pada baris info get, disebelah cmd terdapat 'whoami" sebagai command yg pertama di masukkan
  ![Cuplikan layar 2024-09-20 201730](https://github.com/user-attachments/assets/e47e4463-eed2-4ba9-b2fd-89163e640da1)

  6. Back kemudian cari info yang ada echo"nya di info, kemudian dipaling bawah ada full name request dicopy diantara 20%
  ![Cuplikan layar 2024-09-20 201856](https://github.com/user-attachments/assets/6fe44d89-c425-44ce-96aa-b636fc49e025)

```
cGxzIHJhdGUgc29hbCBpbmkK
```
  7. Hasil decoding: "pls rate soal ini".
  ![Cuplikan layar 2024-09-20 201935](https://github.com/user-attachments/assets/e8e9a441-0b59-4f3c-9304-11839d872f34)

  8. Flag ditemukan
  ![Cuplikan layar 2024-09-20 201132](https://github.com/user-attachments/assets/7d14acb5-d240-4649-a48b-744ea2c91c64)
  ![Cuplikan layar 2024-09-20 201110](https://github.com/user-attachments/assets/49ad0960-d135-4728-a070-728cc5e90f5b)

### Gajah Terbang (Server Record)

  Langkah Penyelesaian:
  1. Untuk mencari DB yang digunakan coba-coba untuk memasukkan port setiap DB yang ada atau disini saya melihat terdapat PGSQL atau PostgreSQL
  ![Cuplikan layar 2024-09-20 204224](https://github.com/user-attachments/assets/71ff2023-d096-4444-b9ec-9e4dc3d5ce40)

  2. Untuk mengetahui port DBnya disini saya menginspect dan merasa banyak port 6969 dan saya merasa itu port DBnya
  ![Cuplikan layar 2024-09-20 204248](https://github.com/user-attachments/assets/1353ae5d-58c3-4c9a-98d1-7c608be26549)

  3. Lakukan slide secara manual dan di baris bawah kemudian follow untuk mengecek isi file yang berisi linux jenis apa dan isi databasenya
  4. Pada file yang di follow, di pojok kiri atas ditemukan credentials untuk user s1gm4 dan nama database sigmaskibidigyatrizzzz.
  5. Mengitung user di db dengan melihat QUERRY SELECT USERS, dan ada 4 user
  6. Ditemukan email admin jojohermawan@gmail.com pada QUERRY SELECT USERS juga
  ![Cuplikan layar 2024-09-20 204316](https://github.com/user-attachments/assets/25cbca6e-ee87-49fa-80e7-564e36dca5fa)

  7. Copy password admin dan dekripsi (9c93ccd78b2076528346216b3b2f701e6) hash password yang menghasilkan admin1234.
  ![Cuplikan layar 2024-09-19 000021](https://github.com/user-attachments/assets/bef818c3-82b8-4f22-800c-3276ba7dcc27)

  8. Flag ditemukan
  ![Cuplikan layar 2024-09-20 203229](https://github.com/user-attachments/assets/d37ae4d9-aeea-4afa-ac7f-b78b85370b60)
  ![Cuplikan layar 2024-09-20 203220](https://github.com/user-attachments/assets/5f75e94e-a4f3-4d2b-904e-02342abdd9a6)
  ![Cuplikan layar 2024-09-20 203205](https://github.com/user-attachments/assets/48523232-6d49-498c-a57c-ed750f0a834b)

### EZ

  Langkah Penyelesaian:
  1. Membuka stream/packet pertama dan follow untuk melihat isinya
     ![image](https://github.com/user-attachments/assets/89bf524c-52ed-47b5-9945-30cc461362b8)
  2. Melihat port berapa yang digunakan oleh stream tersebut
     ![image](https://github.com/user-attachments/assets/9e3ed6a8-821b-41fa-80df-bf11652934ec)
  3. Setelah selesai, maka Flagnya ditemukan
     ![Screenshot (146)](https://github.com/user-attachments/assets/93664775-dec1-4db6-a97b-35efd85a8a68)

### FTP Login

  Langkah Penyelesaian:
  1. Filter packet list dengan keyword "successful", karena pertanyannya yang berhasil login
     ![Screenshot (161)](https://github.com/user-attachments/assets/a387bae2-ed99-43c9-8780-18fa03522a3c)
  2. Setelah menjawab semua maka Flagnya ditemukan
     ![Screenshot (156)](https://github.com/user-attachments/assets/31c77d30-d760-482c-beaa-1e17f8ed1344)
     ![Screenshot 2024-09-18 221534](https://github.com/user-attachments/assets/f35700f4-f506-4570-b2f4-49be94970c1c)

### Packet Barrage

  Langkah Penyelesaian:
  1. Dari data pada soal illegal, stream yang dipilih menggunakan 172.21.88.207 sehingga saya mencoba memasukkan 172.21.80.1 sebagai attackernya
     ![image](https://github.com/user-attachments/assets/2240c06b-c345-48b5-832e-19a72b1963e2)
  2. Stream yang digunakan dipilih dengan filter packet list keywordnya "GET"
  3. Mencoba memasukkan angka 1917 sebagai berapa kali attcaker mencoba brute force
  4. Untuk nama file dan isi file yang disisipkan attacker, saya melihat dalam isi stream tersebut
     ![Screenshot (163)](https://github.com/user-attachments/assets/c6ec9b41-992e-42b2-a26f-e8d327949cea)
  5. Flagnya ditemukan
     ![image](https://github.com/user-attachments/assets/7d43236d-552e-4f7d-aefe-fd80f4d8cc3d)

### Surprise

  Langkah Penyelesaian:
  1. Filter packet list dengan keyword "success"
     ![image](https://github.com/user-attachments/assets/0251fcb1-c7da-49b6-a3b2-5ab525f49a22)
  2. Lalu menjawab dengan jenis FTP (baris pertama isi file) yang digunakan dalam file stream tersebut
     ![image](https://github.com/user-attachments/assets/9e3d754a-6d36-407b-83ec-0520d21e5507)
  3. Dilanjutkan menjawab nama file extension yang ada di dalam dile streamnya
     ![image](https://github.com/user-attachments/assets/6e0f48ed-95a2-48ea-bf77-2d670ada481a)
  4. Next stream menemukan kode lalu di compile dan Flagnya ditemukan
     ![Screenshot (160)](https://github.com/user-attachments/assets/fe857501-d662-4cf9-a5f5-478930e12b5c)
  
      ![image](https://github.com/user-attachments/assets/060921d8-60be-4e96-acc9-1c8cdb73d567)
  
### Malicious

  Langkah Penyelesaian:
  1. Filter dengan keyword **http.request.method == "GET"** dikarenakan get menunjukkan berapa kali attacker mencoba untuk mendapatkan informasi dari server
     ![Screenshot (169)](https://github.com/user-attachments/assets/31aa19df-95d3-4a35-a45b-a12e8a4bf634)
     
     ![Screenshot (170)](https://github.com/user-attachments/assets/d224a6dc-fb2d-4c3a-a6e3-5d4b07f7af49)
  2. Untuk endpointnya saya melihat pada info stream yang menunjukkan **/index.php**
     ![image](https://github.com/user-attachments/assets/27cd5182-411e-48db-a962-630c7aaa017c)
  3. Saya menemukan bahwa stream ini menunjukkan bahwa attacker berhasil masuk sehingga saya mencoba memasukkan length dengan angka 153 dan ternyata berhasil
     ![image](https://github.com/user-attachments/assets/4ec98380-4837-4a50-bcf7-25cff5d23017)
  
     ![image](https://github.com/user-attachments/assets/ea10d2ac-6538-406f-bbaa-be5710ae6e37)
  4. Next stream mengandung kode ASCII yang harus di convert terlebih dahulu
     ![image](https://github.com/user-attachments/assets/014cf942-1f19-42ff-9a93-93ac89ae5a64)
  5. Setelah menjawab pertanyaan dari kode ASCII, maka flagnya ditemukan
     ![image](https://github.com/user-attachments/assets/b84c3afc-2ef5-4c76-ae99-146b109481ff)

### Corporate Breach

1. Saya filter dengan keyword **http** dan follow stream pertamanya yang terdapat indikasi attacker
   ![image](https://github.com/user-attachments/assets/31b7d304-4607-416a-8736-d8939f7296ca)
2. Selanjutnya saya mencoba beberapa email yang saya filter menggunakan packet details **@gmail.com**
   ![image](https://github.com/user-attachments/assets/78d93f8d-4ae0-4f19-ae47-7b77d01bd120)

   ![Screenshot (153)](https://github.com/user-attachments/assets/48323798-c86b-4680-a5c6-3a84e05d2ae0)
4. di dalam stream yang mengandung email tersebut, terlihat password yang digunakan untuk menjawab pertanyaan dan Flagnya ditemukan
   ![Screenshot (154)](https://github.com/user-attachments/assets/3834b9dd-fd46-454e-a9e3-ee119a6cef42)
   
   ![Screenshot (152)](https://github.com/user-attachments/assets/5b42f320-bd72-4157-8e1a-ed14f2c415ba)


