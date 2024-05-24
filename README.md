# Challenge-MIKTI-Team
## Flowchart dan ERD E-Commerce

*Di sini saya akan menjelaskan tentang Flowchart dan ERD yang telah kami buat sebelumnya. Flowchart yang kami buat membantu dalam memvisualisasikan secara sistematis langkah-langkah dalam proses pembuatan website e-commerce, dari sisi penjual yang menambahkan produk hingga pengalaman pelanggan dalam mencari, memilih, dan membeli produk. Sementara itu, ERD kami memberikan pandangan yang jelas tentang struktur database yang diperlukan untuk mendukung fungsionalitas tersebut. Dengan memahami hubungan antara entitas dalam sistem, kami dapat merencanakan dan mengimplementasikan basis data yang efisien dan skalabel untuk proyek kami.*

### Flowchart

![Flowchart E-Commerce](https://github.com/Puputfpspta/Challenge-MIKTI-Team/blob/main/flowchart.png?raw=true)

Flowchart di atas menggambarkan proses pembuatan website secara umum.
*Flowchart ini dimulai dengan Start, kemudian bercabang menjadi dua jalur utama: Penjual dan Pelanggan.*

**Jalur Pelanggan:**

1. **Mencari Produk:**
   Pelanggan mencari produk yang mereka inginkan di website. Mereka dapat menggunakan berbagai kriteria pencarian untuk menemukan produk yang mereka minati.

2. **Barang Ditemukan:**
   Setelah menemukan produk yang mereka cari, pelanggan melihat detailnya, termasuk deskripsi, harga, dan gambar.

3. **Menambahkan ke Keranjang:**
   Jika pelanggan memutuskan untuk membeli produk, mereka dapat menambahkannya ke dalam keranjang belanja. Dan stok produk akan berkurang sementara.

4. **Banyak Produk yang Ingin Dibeli:**
   Pelanggan dapat terus menambahkan produk lain ke dalam keranjang belanja sebelum melanjutkan ke proses checkout.

5. **Proses Pesanan:**
   Pelanggan memasukkan informasi pengiriman, memilih metode pembayaran, dan mengkonfirmasi pesanan sebelum pembayaran.

6. **Konfirmasi:**
   Setelah pesanan berhasil diproses, pelanggan menerima konfirmasi pesanan yang berisi detail tentang produk yang dibeli. Dan stok produk akan berkurang permanen.

7. **Menangani Pembayaran:**
   Sistem website memproses pembayaran dari pelanggan menggunakan berbagai metode pembayaran yang tersedia.

8. **Menyelesaikan Pesanan:**
   Pesanan diproses dan dikirimkan kepada pelanggan. Pelanggan menerima pemberitahuan tentang status pesanan mereka.

**Jalur Penjual:**

1. **Menambahkan Produk:**
   Penjual memulai dengan langkah menambahkan produk baru ke dalam sistem website mereka. Ini melibatkan memasukkan informasi terperinci tentang produk, seperti nama, deskripsi, harga, dan gambar.

2. **Mencari Produk:**
   Penjual dapat mengelola inventaris mereka dan menemukan produk yang spesifik ketika diperlukan, seperti untuk memeriksa stok atau mengedit informasi produk.

3. **Menunggu Pesanan:**
   Penjual menunggu pesanan yang masuk untuk dikirim ke pembeli sebelum menyelesaikan transaksinya.


Flowchart ini memberikan gambaran umum tentang proses pembuatan website dari perspektif penjual yang menambahkan produk hingga perspektif pelanggan yang mencari, memilih, dan membeli produk.

### ERD

![Diagram Entitas Hubungan](https://github.com/Puputfpspta/Challenge-MIKTI-Team/blob/main/ERD_MIKTI.drawio.png?raw=true)

Dari ERD di atas, berikut adalah penjelasan mengenai hubungan antara entitas-entitas yang terdapat dalam sistem:

1. **Users (Pengguna):**
   - Tabel ini menyimpan informasi dasar tentang pengguna, termasuk nama, nomor telepon, email, kata sandi, dan peran mereka.
   - Setiap pengguna memiliki identitas unik (user_id).
   - Pengguna dapat memiliki satu atau lebih peran, yang ditentukan melalui kunci asing role_id_fk yang mengacu pada tabel Roles.

2. **Roles (Peran):**
   - Tabel ini menyimpan informasi tentang peran yang berbeda dalam sistem.
   - Setiap peran memiliki identitas unik (role_id).
   - Sebuah peran dapat dimiliki oleh satu atau lebih pengguna, yang ditentukan melalui hubungan dengan tabel Users.

3. **Products (Produk):**
   - Tabel ini menyimpan informasi tentang produk yang dijual, termasuk nama dan harga.
   - Setiap produk memiliki identitas unik (product_id).

4. **Quantities (Kuantitas):**
   - Tabel ini menyimpan informasi tentang jumlah produk yang dibeli dalam setiap sejarah pembelian.
   - Setiap kuantitas memiliki identitas unik (quantity_id).

5. **Histories (Riwayat Pembelian):**
   - Tabel ini menyimpan riwayat pembelian yang dilakukan oleh pengguna.
   - Setiap history pembelian memiliki informasi tentang pengguna, produk yang dibeli, jumlah yang dibeli, dan harga total.
   - Setiap history pembelian terhubung ke tabel Users, Products, dan Quantities melalui kunci asing (user_id_fk, product_id_fk, dan quantity_id_fk).

Hubungan antara entitas-entitas ini terdiri dari:

- **One-to-Many (Satu-ke-Banyak):**
  - Contoh hubungan satu-ke-banyak adalah antara tabel Users dan tabel Roles.
  - Satu pengguna dapat memiliki satu atau lebih peran.

- **One-to-One (Satu-ke-Satu):**
  - Contoh hubungan satu-ke-satu adalah antara tabel Histories dan tabel Users serta antara tabel Histories dan tabel Products.
  - Setiap sejarah pembelian memiliki satu pengguna yang melakukan pembelian dan satu produk yang dibeli.

## Kontributor

Proyek ini dibuat untuk memenuhi challenge MIKTI dan dibuat oleh satu tim yang terdiri dari:

- Mochammad Yusuf
- Revin Zuhdi Zanzibar
- Sari Andini Putri
- Enrico Zada
- Puput Febi Puspita
