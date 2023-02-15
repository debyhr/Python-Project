# Super Cashier Project
------
Super Cashier Sederhana dengan menggunakan bahasa pemograman Python

## Tujuan Pengerjaan Project
Supermarket Super Indo berencana untuk melakukan modernisasi proses bisnis dengan cara membuat sistem kasir yang self-service. Pada sistem self-service ini, customer bisa langsung memasukkan item yang dibeli, jumlah item, harga item dan fitur-fitur lainnya. Keunggulannya adalah customer yang tidak berada di kota tersebut bisa membeli barang dari supermarket tersbut. Untuk mewujudkan sistem self-service cashier ini, maka project ini dilakukan menggunakan bahasa pemrogaman Python

## Objectives
Self-service cashier ini memiliki fitur-fitur untuk user sebagai berikut:
- input nama, jumlah dan harga item 
- edit nama, jumlah, harga item yang telah diinput
- menamnbah item 
- menghapus beberapa atau semua item (reset) yang ada di keranjang belanja
- menampilkan seluruh item yang ada di keranjang belanja
- mengaplikasikan diskon pada total uang yang harus dibayarkan sesuai syarat
- menampilkan total uang yang harus yang dibayarkan setelah pengaplikasian diskon

## FlowChart
![flowchart](https://user-images.githubusercontent.com/121001516/219148551-3fed2ab8-4d6e-4219-8a54-b4b184408441.png)

## Cara Menggunakan Program
- Module 'cashier.py' terdiri dari Class 'Transaction' yang memuat semua method untuk menjalankan fitur-fitur yang ada di self-service cashier
- Download file module 'cashier.py'
- Untuk menjalankan program self-service cashier ini, dapat dilakukan dengan mengupload file module 'cashier.py' di Jupyter Notebook kemudian impor module 'cashier.py'
- Class Transaction diawali method __init__ yang memiliki atribut-atribut kelas yang diinisialisasi sebagai list kosong. Atribut-atribut ini terdiri atas:
  - list item : nama - nama item yang ada di keranjang belanja user
  - list_jumlah_item : jumlah dari setiap item yang ada di keranjang belanja user
  - list_harga_item : harga dari setiap item yang ada di keranjang belanja user
  - list_harga_total : total harga dari setiap item. Didapat dengan mengkalikan jumlah item dengan harga item
  - df : dataframe yang dihasilkan dari dictionary yang terdiri dari list_item, list_jumlah_item, list_harga_item, list_harga_total 
 
    ![image](https://user-images.githubusercontent.com/121001516/218315193-4cb7a07c-1f80-480c-bd91-f21d4954395a.png)

- Berikut adalah methods yang terdapat di Class 'Transaction':
  - Method basket untuk menambahkan item ke keranjang belanja. Sebelum input nama, jumlah dan harga item, user akan ditanya jumlah jenis item yang akan dibayar. Setelah semua item sudah diinput, maka akan keluar output dataframe nama, jumlah, harga/item dan total harga dari semua item.
  
    ![image](https://user-images.githubusercontent.com/121001516/218343215-c992b456-65ac-42f6-9a92-7bdeac4149a6.png)
    
  - Method update_items untuk mengedit item yang ada di keranjang belanja. User dibeli 4 pilihan edit. Untuk mengedit item, user harus menginput nomor urut item sesuai dengan yang tertera pada tabel item di keranjang belanja

    ![image](https://user-images.githubusercontent.com/121001516/218343254-ef3dc291-5fcc-4d43-9a4f-e61a05846937.png)
    
    ![image](https://user-images.githubusercontent.com/121001516/218343338-a0d011d0-2e2d-49df-b263-9b19fa642bf0.png)
    
    ![image](https://user-images.githubusercontent.com/121001516/218343368-fd8a63ee-feb2-4005-b002-9ae34080b092.png)

  - Method delete_items untuk menghapus item yang ada di keranjang belanja. User dibeli 2 pilihan delete (delete semua item/reset dan delete beberapa item). Untuk menghapus item, user harus menginput nomor urut item yang ingin dihapus sesuai dengan yang tertera pada tabel item di keranjang belanja
    
    ![image](https://user-images.githubusercontent.com/121001516/218343407-5980a705-ec5a-48d2-8995-ba09495dae53.png)
    ![image](https://user-images.githubusercontent.com/121001516/218343441-53658485-1670-494c-9963-8284d2ab59d8.png)

  - Method check_order untuk mengecek item apa saja yang ada di keranjang belanja user
    
    ![image](https://user-images.githubusercontent.com/121001516/218343473-b4f7b087-6c12-4f66-be7b-ad852ccc2540.png)

  - Method total_price untuk menampilkan total belanja yang harus dibayarkan user. Nominal diskon yang didapatkan user berdasarkan total belanja. User juga dapat mengetahui jumlah diskon yang mereka dapatkan
    
    ![image](https://user-images.githubusercontent.com/121001516/218343486-6c628d92-9f57-443b-ab77-326236c8a34a.png)
    
   - Running class dan methods
   
     ![image](https://user-images.githubusercontent.com/121001516/218343505-b5cd7d7c-237a-4b53-825f-5c5d3be23fc2.png)

## Hasil Test Case
1. Sistem akan menanyakan user berapa jenis item belanjaan mereka yang akan bayar. Kemudian customer menginput nama, jumlah serta harga per item sebanyak jumlah jenis item. Output dari function ini adalah dataframe yang berisi rincian item user serta total harga setiap jenis item

   ![image](https://user-images.githubusercontent.com/121001516/218479671-c234dd0d-d16e-4432-9e2e-76b6794a4e2b.png)


2. Sistem akan menunjukkan dataframe rincian item belanja user kemudian sistem akan menanyakan apakah ada item belanja yang ingin diganti. Jika user memilih "yes" maka sistem akan kembali menanyakan 4 pilihan edit item belanja. Rincian item belanja user akan kembali diperlihatkan setelah proses edit selesai. Jika user menjawab "no" maka sistem akan melanjutkan ke fitur selanjutnya (delete_items). 
	 
	 - **Menambah item.** User akan ditanya apakah ingin menambah item belanja. Jika user menjawab "yes" maka sistem akan bertanya jumlah jenis item yang ingin ditambah, kemudian user akan menginput nama, jumlah serta harga per item yang ingin ditambahkan sebanyak jumlah jenis item.
	 ![image](https://user-images.githubusercontent.com/121001516/218480873-3eafabe9-02f2-4dd1-a56b-37e3a2a427db.png)
	 - **Mengganti nama item**. User akan ditanya apakah ingin mengubah nama item belanja yang telah diinput sebelumnya. Jika user menjawab "yes" maka sistem akan bertanya jumlah jenis item yang namanya ingin diubah, kemudian user akan ditanya no. urutan/index item tersebut. Setelah itu, user diminta untuk input nama item baru untuk index tersebut. 
	 
	   ![image](https://user-images.githubusercontent.com/121001516/218487350-9d122c5f-1697-49a0-8268-d647b92db793.png)
	 - **Mengganti jumlah item**. User akan ditanya apakah ingin mengubah jumlah item belanja yang telah diinput sebelumnya. Jika user menjawab "yes" maka sistem akan bertanya jumlah jenis item yang jumlahnya ingin diubah, kemudian user akan ditanya no. urutan/index item tersebut. Setelah itu, user diminta untuk input jumlah item baru untuk index tersebut.
	   ![image](https://user-images.githubusercontent.com/121001516/218568242-3db340c8-98f0-4f20-97be-20e67674289a.png)
 
	 - **Mengganti harga item**. User akan ditanya apakah ingin mengubah harga item belanja yang telah diinput sebelumnya. Jika user menjawab "yes" maka sistem akan bertanya jumlah jenis item yang harganya ingin diubah, kemudian user akan ditanya no. urutan/index item tersebut. Setelah itu, user diminta untuk input harga item baru untuk index tersebut.
	   ![image](https://user-images.githubusercontent.com/121001516/218569685-22b6905e-6326-4a3e-90f8-01d3afe14e65.png)

3. Sistem akan menunjukkan dataframe rincian item belanja user kemudian sistem akan menanyakan apakah ada item belanja yang ingin dihapus. Jika user memilih "yes" maka sistem akan kembali menanyakan 2 pilihan hapus item belanja. Jika user menjawab "no" maka sistem akan melanjutkan ke fitur selanjutnya (check_orders).

	- **Hapus beberapa item**. User akan ditanya apakah ingin menghapus satu atau lebih item belanja yang ada di sistem. Jika user menjawab "yes" maka sistem akan bertanya jumlah jenis item yang ingin dihapus, kemudian user akan ditanya no. urutan/index item tersebut. Rincian item belanja user akan kembali diperlihatkan setelah proses penghapusan item selesai.
	 ![image](https://user-images.githubusercontent.com/121001516/218579006-40cfecbd-1c83-4a0b-9612-91cdaebb09fd.png)

	- **Hapus semua item (reset)**. User akan ditanya apakah ingin menghapus semua item belanja yang ada di sistem. Jika user menjawab "yes" maka sistem akan menghapus semua item dan sistem berhenti.
	 ![image](https://user-images.githubusercontent.com/121001516/218579413-d540b088-16c0-4c41-a0f5-6e7b0e8788ba.png)

5. Sebelum check out, sistem akan bertanya apakah user ingin melihat semua item yang telah dipesan.  
	- **Jika user memilih "yes"** maka akan ditampilkan tabel item belanja user.
	 ![image](https://user-images.githubusercontent.com/121001516/218581114-5ed3c4ee-3e43-4370-918d-986c208459aa.png)

	- **Jika user memilih "no"** maka sistem akan melanjutkan ke fitur selanjutnya (total_price)
7. Sistem memproses total belanja user dan mengaplikasikan diskon jika total belanja user mencapi syarat diskon. 
   ![image](https://user-images.githubusercontent.com/121001516/218581763-6b523334-990e-435e-8f90-f6daa1c80ea8.png)

## Kesimpulan
Kelebihan dari sistem self-service cashier Supermarket Super Indo yaitu, sistem ini memiliki fitur-fitur yang memungkinkan user untuk:
1. mengedit nama / kuantitas / harga item belanjaan mereka tanpa harus menghapus 1 row pesanan item tersebut. 
2. menambah item belanja tanpa harus keluar sistem dan mengulang proses dari awal
3. menghapus beberapa item yang diinginkan tanpa harus menghapus semua item di keranjang belanja 
4. menghapus semua item belanja dan keluar dari sistem dengan mudah
5. mengecek rincian belanja mereka di awal dan akhir segala fitur. Di akhir proses delete, edit dan pembayaran akan ditampilkan rincian item-item belanja mereka yang terbaru. 
6. mengetahui jumlah diskon yang mereka dapatkan sesuai syarat yang berlaku. 

Kekurangan dari sistem self-service cashier Supermarket Super Indo yaitu:
1. proses input item belanja yang banyak dapat memakan waktu yang lama karena dilakukan secara manual mulai dari nama, kuantitas dan harga. Akan lebih mudah, jika diberi list item-item yang dijual di supermarket beserta harga nya. Dengan cara itu, user bisa menginput no.urutan / index dari item yang diinginkan berdasarkan list, kemudian dengan IF statements dan loop bisa dicari nama item serta harga per item tersebut. Jadi user hanya perlu menginput no.urut dan kuantitas.

