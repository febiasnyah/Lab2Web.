# Pratikum 2: CSS Dasar

README ini disusun sebagai laporan praktikum lengkap. Semua langkah mengikuti modul praktikum (praktikum 2) dan dilengkapi screenshot hasil kerja.
# 1. Membuat dokumen HTML dasar (lab2_css_dasar.HTML)
Buat file HTML dengan struktur dasar berikut:
<img width="1920" height="1080" alt="Cuplikan layar 2025-09-29 121559" src="https://github.com/user-attachments/assets/a2611785-12f2-436b-b97d-695ca2eeb06c" />
Penjelasan : <!DOCTYPE html> untuk mode standar, meta viewport untuk responsif, dan < link > akan menghubungkan file CSS eksternal.

# 2. Menambahkan CSS Internal
Tambahkan di dalam < head >:
<img width="1920" height="1080" alt="Cuplikan layar 2025-09-29 122727" src="https://github.com/user-attachments/assets/a8b28034-1cad-49ee-b787-5e60804770ba" />
Penjelasan : Internal CSS cepat untuk testing. Namun untuk laporan, gunakan CSS eksternal agar terpisah dari markup.

# 3. Menambahkan Inline CSS
Contoh pada paragraf: 
< p style="text-align: center; color: #ccd8e4;">Paragraf dengan inline style </p>
<img width="1920" height="1080" alt="Cuplikan layar 2025-09-29 123233" src="https://github.com/user-attachments/assets/ce484240-d836-49fe-ae8b-57e45d6a349f" />
Penjelasan: Inline CSS hanya mempengaruhi elemen tersebut. Biasanya dipakai untuk override cepat.

# 4. Membuat CSS Eksternal
Buat file css/style_eksternal.css dan isi contoh berikut:
<img width="1920" height="1080" alt="Cuplikan layar 2025-09-29 183234" src="https://github.com/user-attachments/assets/3895c5fc-46b8-4ea5-ac6a-be3ec45aa17c" />
Penjelasan: External CSS memudahkan pemeliharaan dan diterapkan ke banyak halaman.

Kemudian tambahkan tag < link>  untuk merujuk file CSS yang sudah dibuat pada bagian <head>
<img width="1920" height="1080" alt="Cuplikan layar 2025-09-29 124323" src="https://github.com/user-attachments/assets/5c58aa8e-86f2-42c9-8a1f-21d6193b0484" />

# 5. Menambahkan Selector ID & Class
ID: #intro { ... } — untuk elemen unik.

Class: .button { ... } — untuk gaya yang bisa dipakai berulang.
<img width="1920" height="1080" alt="Cuplikan layar 2025-09-29 125705" src="https://github.com/user-attachments/assets/c8cd03b4-61ff-41c1-95cf-fa31738c1a43" />

# Pertanyaan dan Tugas
1. Lakukan eksperimen dengan mengubah dan menambah properti dan nilai pada kode CSS dengan mengacu pada CSS Cheat Sheet yang diberikan pada file terpisah dari modul ini.

JAWAB:

<img width="1920" height="1080" alt="Cuplikan layar 2025-09-29 193136" src="https://github.com/user-attachments/assets/f862ee60-5976-4366-bf12-fe6cc9d3d3df" />


2. Apa perbedaan pendeklarasian CSS elemen h1 (...) dengan #intro h1 (...)? berikan penjelasannya!

JAWAB:

- h1 {…} → berlaku untuk semua elemen < h1 > dalam dokumen.
- #intro h1 {…} → hanya berlaku pada elemen < h1 > yang ada di dalam elemen dengan id intro.
- Kesimpulan: #intro h1 lebih spesifik daripada h1 biasa. Jika keduanya ada, maka gaya dari #intro h1 akan diterapkan untuk < h1 > di dalam #intro.

  
3. Apabila ada deklarasiCSS secara internal, lalu ditambahkan CSS eksternal dan inline CSS pada elemen yang sama. Dekslarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya!

JAWAB:

- CSS memiliki hirarki prioritas (specificity).
- Urutannya:
  
  1. Inline CSS (ditulis langsung di atribut style elemen HTML) → paling tinggi.
  2. Internal CSS (ditulis dalam tag <style> di file HTML).
  3. Eksternal CSS (ditulis di file .css yang dihubungkan dengan < link >).

Jika ada konflik gaya (misalnya warna teks berbeda), maka yang digunakan adalah inline CSS, karena memiliki prioritas tertinggi.

Contoh Kode:
<img width="1920" height="1080" alt="Cuplikan layar 2025-09-29 195008" src="https://github.com/user-attachments/assets/be29843f-1304-4acd-8991-8a19c41a9bbb" />
Hasil tampilan:

- Teks paragraf akan berwarna merah, karena aturan inline CSS mengalahkan internal dan eksternal.

- Jadi kesimpulannya: Inline > Internal > Eksternal.

4. Pada sebuah elemen HTML terdapat ID dan Class, apabila masing-masing selector tersebut terdapat deklarasi CSS, maka deklarasi manakah yang akan ditampilkan pada browser? berikan penjelasan dan contohnya! ( < p id= "paragraf-1" class="text-paragraf" > )

JAWAB:

- CSS memiliki aturan specificity (tingkat kekhususan selector).
- ID selector (#id) lebih spesifik daripada Class selector (.class).
- Jadi, jika sebuah elemen HTML memiliki ID dan Class, dan keduanya mendeklarasikan properti yang sama, maka aturan dari ID yang akan diterapkan.

Contoh Kode CSS:
<img width="1920" height="1080" alt="Cuplikan layar 2025-09-29 200212" src="https://github.com/user-attachments/assets/16b26fa8-b9da-448f-8265-0bd47fe6fb88" />

Contoh kode HTML:
<img width="1920" height="1080" alt="Cuplikan layar 2025-09-29 200313" src="https://github.com/user-attachments/assets/ee29cc7e-15b0-402b-9ffd-107bee6b799e" />

Hasil Tampilan:

- Teks akan berwarna merah, karena selector #paragraf-1 (ID) lebih kuat dibanding .text-paragraf (Class).

- Kesimpulan: Jika ada konflik properti, ID akan menang dibanding Class karena tingkat kekhususannya lebih tinggi.
