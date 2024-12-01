# labpy6
# Praktikum6
# penjelasan Praktikum6
Program ini dibuat untuk mengelola data mahasiswa dengan cara yang sederhana menggunakan Python. 
Data mahasiswa disimpan dalam bentuk daftar (list), di mana setiap elemen adalah sebuah kamus (dictionary) yang menyimpan nama dan nilai mahasiswa.

Ada empat fungsi utama dalam program ini. Pertama, fungsi tambah untuk menambahkan data mahasiswa ke daftar. Kedua, fungsi tampilkan 
digunakan untuk melihat semua data yang sudah dimasukkan. Ketiga, fungsi hapus memungkinkan pengguna menghapus data mahasiswa tertentu berdasarkan nama.
Keempat, fungsi ubah berguna untuk memperbarui nilai mahasiswa yang sudah ada.

Selain itu, program ini memiliki menu interaktif yang memungkinkan pengguna memilih tindakan yang diinginkan, 
seperti menambah data, melihat data, menghapus data, mengubah data, atau keluar dari program.
Pengguna cukup memasukkan pilihan angka sesuai dengan menu yang tersedia. Program akan terus berjalan sampai pengguna memilih opsi keluar.

Data yang dimasukkan hanya disimpan selama program berjalan, sehingga tidak akan tersimpan secara permanen.
Program ini cocok untuk latihan sederhana dalam pengelolaan data menggunakan Python.

# Flowchart
![image](https://github.com/user-attachments/assets/b2edac75-e6e6-48ec-85da-b981000d0702)
# codingan
 mahasiswa = []  # Daftar untuk menyimpan data mahasiswa

 def tambah(nama, nilai):
    """Menambahkan data mahasiswa ke dalam daftar."""
    mahasiswa.append({"nama": nama, "nilai": nilai})
    print(f"Data {nama} berhasil ditambahkan.")

 def tampilkan():
    """Menampilkan semua data mahasiswa."""
    if not mahasiswa:
        print("Tidak ada data mahasiswa.")
        return
    print("Daftar Nilai Mahasiswa:")
    for index, mhs in enumerate(mahasiswa, start=1):
        print(f"{index}. Nama: {mhs['nama']}, Nilai: {mhs['nilai']}")

 def hapus(nama):
    """Menghapus data mahasiswa berdasarkan nama."""
    global mahasiswa
    mahasiswa = [mhs for mhs in mahasiswa if mhs["nama"] != nama]
    print(f"Data {nama} berhasil dihapus.")

 def ubah(nama, nilai_baru):
    """Mengubah data mahasiswa berdasarkan nama."""
    for mhs in mahasiswa:
        if mhs["nama"] == nama:
            mhs["nilai"] = nilai_baru
            print(f"Data {nama} berhasil diubah menjadi nilai {nilai_baru}.")
            return
    print(f"Data {nama} tidak ditemukan.")

 def menu():
    """Menampilkan menu utama."""
    while True:
        print("\nMenu:")
        print("1. Tambah Data")
        print("2. Tampilkan Data")
        print("3. Hapus Data")
        print("4. Ubah Data")
        print("5. Keluar")
        pilihan = input("Pilih opsi (1-5): ")

        if pilihan == '1':
            nama = input("Masukkan nama mahasiswa: ")
            nilai = input("Masukkan nilai mahasiswa: ")
            tambah(nama, nilai)
        elif pilihan == '2':
            tampilkan()
        elif pilihan == '3':
            nama = input("Masukkan nama mahasiswa yang ingin dihapus: ")
            hapus(nama)
        elif pilihan == '4':
            nama = input("Masukkan nama mahasiswa yang ingin diubah: ")
            nilai_baru = input("Masukkan nilai baru: ")
            ubah(nama, nilai_baru)
        elif pilihan == '5':
            print("Terima kasih!")
            break
        else:
            print("Pilihan tidak valid. Silakan coba lagi.")

  if __name__ == "__main__":
      menu()


# penjelasan 
Penjelasan Berikut adalah penjelasan mengenai kode yang Anda berikan, yang merupakan program sederhana untuk mengelola data mahasiswa. Program ini memungkinkan pengguna untuk menambah, menampilkan, menghapus, dan mengubah data mahasiswa. Mari kita bahas setiap bagian dari kode tersebut:
# 1. Daftar untuk menyimpan data mahasiswa
   Mahasiswa = []
  

