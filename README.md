# Super Cashier Project
------
Super Cashier Sederhana dengan menggunakan bahasa pemograman Python

## Tujuan Pengerjaan Project
Suatu supermarket besar di salah satu kota Indonesia berencana untuk melakukan modernisasi proses bisnis dengan cara membuat sistem kasir yang self-service. Pada sistem self-service ini, customer bisa langsung memasukkan item yang dibeli, jumlah item, harga item dan fitur-fitur lainnya. Keunggulannya adalah customer yang tidak berada di kota tersebut bisa membeli barang dari supermarket tersbut. Untuk mewujudkan sistem self-service cashier ini, maka project ini dilakukan menggunakan bahasa pemrogaman Python

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
  
    ![image](https://user-images.githubusercontent.com/121001516/218328028-fb38b981-e361-4c2a-9a82-416aa3497db2.png)

    
  - Function update_items untuk mengedit item yang ada di keranjang belanja. User dibeli 4 pilihan edit. Untuk mengedit item, user harus menginput nomor urut item sesuai dengan yang tertera pada tabel item di keranjang belanja

    ![image](https://user-images.githubusercontent.com/121001516/218328081-071b6363-2e04-4cc3-8fc0-452a70a5242e.png)
    
    ![image](https://user-images.githubusercontent.com/121001516/218328139-558e5815-1b34-41c8-9b62-30ffd7a950ec.png)
    
    ![image](https://user-images.githubusercontent.com/121001516/218328185-8999b3b2-ff25-4bc7-ab7b-31a916fa9525.png)

