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
![1](https://user-images.githubusercontent.com/121001516/218312092-e8f4c23a-6a8b-477f-a81e-c49b70621a0d.png)
![2](https://user-images.githubusercontent.com/121001516/218312105-7ba8bc6a-863b-482c-badc-48d6a39e138c.png)
![3](https://user-images.githubusercontent.com/121001516/218312114-f31cac4b-a1dd-4932-b726-7567b227d852.png)
![4](https://user-images.githubusercontent.com/121001516/218312123-190d1a88-0103-4f1b-a3ce-8b417cb9d3ac.png)

## Cara Menggunakan Program
- Module 'cashier.py' terdiri dari Class 'Transaction' yang memuat semua function untuk menjalankan fitur-fitur yang ada di self-service cashier
- Download file module 'cashier.py'
- Untuk menjalankan program self-service cashier ini, dapat dilakukan dengan mengupload file module 'cashier.py' di Jupyter Notebook kemudian impor module 'cashier.py'
- Class Transaction diawali method __init__ yang memiliki atribut-atribut kelas yang diinisialisasi sebagai list kosong. Atribut-atribut ini terdiri atas:
  - list item : nama - nama item yang ada di keranjang belanja user
  - list_jumlah_item : jumlah dari setiap item yang ada di keranjang belanja user
  - list_harga_item : harga dari setiap item yang ada di keranjang belanja user
  - list_harga_total : total harga dari setiap item. Didapat dengan mengkalikan jumlah item dengan harga item
  - df : dataframe yang dihasilkan dari dictionary yang terdiri dari list_item, list_jumlah_item, list_harga_item, list_harga_total 
 
    ![image](https://user-images.githubusercontent.com/121001516/218315193-4cb7a07c-1f80-480c-bd91-f21d4954395a.png)

- Berikut adalah function-function yang terdapat di Class 'Transaction':
  - Function basket untuk menambahkan item ke keranjang belanja. Sebelum input nama, jumlah dan harga item, user akan ditanya jumlah jenis item yang akan dibayar. Setelah semua item sudah diinput, maka akan keluar output dataframe nama, jumlah, harga/item dan total harga dari semua item.
  
    ![image](https://user-images.githubusercontent.com/121001516/218343215-c992b456-65ac-42f6-9a92-7bdeac4149a6.png)
    
  - Function update_items untuk mengedit item yang ada di keranjang belanja. User dibeli 4 pilihan edit. Untuk mengedit item, user harus menginput nomor urut item sesuai dengan yang tertera pada tabel item di keranjang belanja

    ![image](https://user-images.githubusercontent.com/121001516/218343254-ef3dc291-5fcc-4d43-9a4f-e61a05846937.png)
    
    ![image](https://user-images.githubusercontent.com/121001516/218343338-a0d011d0-2e2d-49df-b263-9b19fa642bf0.png)
    
    ![image](https://user-images.githubusercontent.com/121001516/218343368-fd8a63ee-feb2-4005-b002-9ae34080b092.png)

  - Function delete_items untuk menghapus item yang ada di keranjang belanja. User dibeli 2 pilihan delete (delete semua item/reset dan delete beberapa item). Untuk menghapus item, user harus menginput nomor urut item yang ingin dihapus sesuai dengan yang tertera pada tabel item di keranjang belanja
    
    ![image](https://user-images.githubusercontent.com/121001516/218343407-5980a705-ec5a-48d2-8995-ba09495dae53.png)
    ![image](https://user-images.githubusercontent.com/121001516/218343441-53658485-1670-494c-9963-8284d2ab59d8.png)

  - Function check_order untuk mengecek item apa saja yang ada di keranjang belanja user
    
    ![image](https://user-images.githubusercontent.com/121001516/218343473-b4f7b087-6c12-4f66-be7b-ad852ccc2540.png)

  - Function total_price untuk menampilkan total belanja yang harus dibayarkan user. Nominal diskon yang didapatkan user berdasarkan total belanja. User juga dapat mengetahui jumlah diskon yang mereka dapatkan
    
    ![image](https://user-images.githubusercontent.com/121001516/218343486-6c628d92-9f57-443b-ab77-326236c8a34a.png)
    
   - Running class dan function
   
     ![image](https://user-images.githubusercontent.com/121001516/218343505-b5cd7d7c-237a-4b53-825f-5c5d3be23fc2.png)

## Hasil Test Case
1. Sistem akan menanyakan user berapa jenis item belanjaan mereka yang akan bayar. Kemudian customer menginput nama, jumlah serta harga per item sebanyak jumlah jenis item. Output dari function ini adalah dataframe yang berisi rincian item user serta total harga setiap jenis item

   ![image](https://user-images.githubusercontent.com/121001516/218479671-c234dd0d-d16e-4432-9e2e-76b6794a4e2b.png)


2. Sistem akan menunjukkan dataframe rincian item belanja user kemudian sistem akan menanyakan apakah ada item belanja yang ingin diganti. Jika user memilih "yes" maka sistem akan kembali menanyakan 4 pilihan edit item belanja. Rincian item belanja user akan kembali diperlihatkan setelah proses edit selesai. Jika user menjawab "no" maka sistem akan melanjutkan ke fitur selanjutnya (delete_items). 
	 
	 - **Menambah item.** User akan ditanya apakah ingin menambah item belanja. Jika user menjawab "yes" maka sistem akan bertanya jumlah jenis item yang ingin ditambah, kemudian user akan menginput nama, jumlah serta harga per item yang ingin ditambahkan sebanyak jumlah jenis item.
	 ![image](https://user-images.githubusercontent.com/121001516/218480873-3eafabe9-02f2-4dd1-a56b-37e3a2a427db.png)
	 - **Mengganti nama item**. User akan ditanya apakah ingin mengubah nama item belanja yang telah diinput sebelumnya. Jika user menjawab "yes" maka sistem akan bertanya jumlah jenis item yang namanya ingin diubah, kemudian user akan ditanya no. urutan/index item tersebut. Setelah itu, user diminta untuk input nama item baru untuk index tersebut. 
	 
	   ![image](https://user-images.githubusercontent.com/121001516/218487350-9d122c5f-1697-49a0-8268-d647b92db793.png)
	 - **Mengganti jumlah item**, User akan ditanya apakah ingin mengubah jumlah item belanja yang telah diinput sebelumnya. Jika user menjawab "yes" maka sistem akan bertanya jumlah jenis item yang jumlahnya ingin diubah, kemudian user akan ditanya no. urutan/index item tersebut. Setelah itu, user diminta untuk input jumlah item baru untuk index tersebut.
	 - 
	 - **Mengganti harga item**
      

   
4. 
