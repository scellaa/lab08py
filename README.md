# PRATIKUM PERTEMUAN 12
### LAB 08 PYTHON

#### NAMA: MAYSCELA HERLIYAWATI
#### NIM: 312510371
#### KELAS: TI.25.C5
______________________________________

#### Flowchart picture 

<img width="1018" height="1201" alt="Diagram pemrog 12 drawio" src="https://github.com/user-attachments/assets/2b9bce97-bc9f-4084-9120-febfbb619d0c" />

### Output dari code 

<img width="1114" height="548" alt="Screenshot 2025-12-07 124608" src="https://github.com/user-attachments/assets/9a82ca30-a185-47e6-a0ff-5b14eb24e085" />

<img width="1003" height="643" alt="Screenshot 2025-12-07 124627" src="https://github.com/user-attachments/assets/488d2718-7fad-49c3-aedb-1b0930c322be" />


<img width="1098" height="686" alt="Screenshot 2025-12-07 124655" src="https://github.com/user-attachments/assets/30b36935-cb6e-4ee7-b9af-779e0a8fea75" />



### Penjelasan Kode

#### 1. Kelas Mahasiswa dan Inisialisasi Data
Pada bagian awal, kelas Mahasiswa dibuat untuk menampung seluruh fungsi pengelolaan data. Di dalam method __init__, 
dibentuk sebuah list kosong bernama self.data yang akan digunakan untuk menyimpan semua data mahasiswa dalam bentuk dictionary. Dengan struktur ini,     
setiap data mahasiswa yang ditambah, diubah, atau dihapus akan terorganisir rapi dalam satu variabel.
#### 2. Method tambah() untuk Menambahkan Data 
Method tambah() bertugas menerima data mahasiswa berupa nama, NIM, serta nilai tugas, UTS, dan UAS. Setelah menerima input, method ini menghitung nilai akhir berdasarkan bobot 
penilaian (30% tugas, 35% UTS, dan 35% UAS). Semua data tersebut kemudian dikemas ke  dalam dictionary dan dimasukkan ke list self.data. 
Sebagai penanda keberhasilan, program menampilkan pesan bahwa data telah berhasil ditambahkan ke daftar.
#### 3. Method hapus() untuk Menghapus Data Mahasiswa 
Method ini mencari data berdasarkan nama mahasiswa yang diberikan oleh pengguna. Pencarian dilakukan secara case-insensitive agar huruf besar atau kecil tidak mempengaruhi hasil. 
Jika data ditemukan, dictionary mahasiswa tersebut dihapus dari list using remove(). Jika tidak ditemukan, program memberikan informasi bahwa data tidak tersedia. 
Fungsi ini memastikan daftar data tetap bersih dari entri yang tidak lagi dibutuhkan.
#### 4. Method ubah() untuk Memperbarui Data Mahasiswa 
Method ini digunakan ketika pengguna ingin mengubah sebagian atau seluruh data mahasiswa. Program mencari nama mahasiswa terlebih dahulu. Jika ditemukan, 
setiap nilai baru yang diberikan pengguna (baik itu NIM, nilai tugas, nilai UTS, maupun nilai UAS) akan menggantikan nilai lama. Setelah itu, nilai akhir juga dihitung ulang. Namun, dalam kode asli 
terdapat kesalahan pada perhitungan nilai akhir karena ada operator yang hilang. Secara konsep, method ini dirancang agar perubahan data bisa dilakukan fleksibel tanpa harus mengganti semua informasi.
##### 5. Method tampilkan() untuk Melihat Data Mahasiswa 
Method tampilkan() berfungsi menampilkan seluruh daftar mahasiswa dengan format tabel yang rapi. Bagian awal menampilkan header tabel beserta garis pemisah. 
Apabila tidak ada data sama sekali, program akan menampilkan pesan bahwa data masih kosong. Jika ada, data ditampilkan satu per satu menggunakan enumerate() sehingga setiap mahasiswa memiliki nomor urut. 
Format yang digunakan memastikan tampilan tabel mudah dibaca dan terstruktur.
#### 6. Program Utama dan Menu Berulang 
Setelah kelas selesai, program memasuki loop while True yang berfungsi sebagai menu utama. Di sini pengguna diberi pilihan: melihat data, menambah data, mengubah data, menghapus data, atau keluar dari program. 
Setiap pilihan akan memanggil method yang sesuai di kelas Mahasiswa. Menu ini terus berulang hingga pengguna memilih keluar. Bagian ini juga memiliki validasi input angka menggunakan try/except agar
program tidak crash ketika pengguna memasukkan nilai yang bukan angka.

Secara keseluruhan, program ini adalah implementasi dari fitur CRUD (Create, Read, Update, Delete) untuk pengolahan data mahasiswa. Setiap fungsinya terpisah dengan jelas di dalam kelas Mahasiswa, 
sementara interaksi dengan pengguna diatur oleh menu utama. Program ini sederhana namun lengkap untuk simulasi pengolahan data berbasis teks.
