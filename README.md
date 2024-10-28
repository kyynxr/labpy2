# LAPORAN 3

# PROGRAM TIKET BIOSKOP

![gambar](https://github.com/kyynxr/labpy2/blob/8a3e388c52122f706a2959e29e404f71c232b20d/RIZKY.jpg)

python
# Fungsi untuk menghitung harga tiket
def hitung_harga_tiket():
    # Harga tiket
    harga_reguler = 50000
    harga_vip = 100000
    diskon_member = 0.20  # Diskon 20%

    # Meminta input dari pengguna
    tipe_tiket = input("Masukkan tipe tiket (reguler/VIP): ").strip().lower()
    status_member = input("Apakah Anda memiliki kartu member? (ya/tidak): ").strip().lower()

    # Menentukan harga berdasarkan tipe tiket
    if tipe_tiket == "reguler":
        harga_tiket = harga_reguler
    elif tipe_tiket == "vip":
        harga_tiket = harga_vip
    else:
        print("Tipe tiket tidak valid!")
        return

    # Menghitung total harga dengan diskon jika berlaku
    if status_member == "ya":
        total_harga = harga_tiket * (1 - diskon_member)
    elif status_member == "tidak":
        total_harga = harga_tiket
    else:
        print("Status member tidak valid!")
        return

    # Menampilkan total harga
    print(f"Total harga yang harus dibayar: Rp{total_harga:.2f}")

# Memanggil fungsi
hitung_harga_tiket()


Program ini akan menentukan harga pesanan tiket bioskop, Yang reguler/Vip, dan jika Vip harga 100.000, dan jika reguler 80.0000, dan jika memiliki kartu member pelanggan tersebut akan mendapatkan diskon 20%

 python
 harga_reguler = 50000
    harga_vip = 100000


Untuk menentukan harga tiket tersebut

 python
tipe_tiket = input("Masukkan tipe tiket (reguler/VIP): ").strip().lower()
    status_member = input("Apakah Anda memiliki kartu member? (ya/tidak): ").strip().lower()


Pengguna diminta untuk memasukkan tipe tiket yang mereka inginkan, bisa "reguler" atau "VIP", Pengguna juga diminta untuk menjawab apakah mereka memiliki kartu member, dengan pilihan "ya" atau "tidak"

 python
if tipe_tiket == "reguler":
        harga_tiket = harga_reguler
    elif tipe_tiket == "vip":
        harga_tiket = harga_vip
    else:
        print("Tipe tiket tidak valid!")
        return


Jika tipe tiket adalah "reguler", harga tiket akan diatur menjadi harga_reguler (Rp50.000), Jika tipe tiket adalah "VIP", harga tiket akan diatur menjadi harga_vip (Rp100.000), Jika tipe tiket yang dimasukkan tidak valid, fungsi akan menampilkan pesan error dan menghentikan proses

 python
if status_member == "ya":
        total_harga = harga_tiket * (1 - diskon_member)
    elif status_member == "tidak":
        total_harga = harga_tiket
    else:
        print("Status member tidak valid!")
        return


Jika pengguna adalah member (status_member == "ya"), harga tiket akan dikurangi diskon 20%, Jika pengguna bukan member (status_member == "tidak"), harga tiket tetap sama tanpa pengurangan, Jika input untuk status member tidak valid, misalnya selain "ya" atau "tidak", fungsi akan menampilkan pesan error dan menghentikan eksekusi

 python
print(f"Total harga yang harus dibayar: Rp{total_harga:.2f}")

Setelah menghitung total harga, anda dapat langsung menjalankan fungsinya

Hasil program tersebut:

![python1](https://github.com/user-attachments/assets/3748410e-b384-4e6f-a4da-60027bdd0dbe)

Code program tersebut:

![python2](https://github.com/user-attachments/assets/30e099c7-f7e5-401b-9877-cfd641f2a5d5)

3Dan ini flowchart nya

![Gambar](https://github.com/user-attachments/assets/4f18d40d-0f74-459b-8d86-664b0dacdff7)

# Prorgam Kalkulator Sederhana

![Gambar](https://github.com/user-attachments/assets/64d66b05-b414-4780-940c-5ac28bfe814d)

python
# Fungsi untuk kalkulator sederhana
def kalkulator():
    # Meminta input dari pengguna
    angka1 = float(input("Masukkan angka pertama: "))
    angka2 = float(input("Masukkan angka kedua: "))
    operator = input("Masukkan operator (+, -, *, /): ").strip()

# Menghitung hasil berdasarkan operator yang dipilih
    if operator == "+":
        hasil = angka1 + angka2
    elif operator == "-":
        hasil = angka1 - angka2
    elif operator == "*":
        hasil = angka1 * angka2
    elif operator == "/":
        if angka2 != 0:
            hasil = angka1 / angka2
        else:
            print("Error: Pembagian dengan nol tidak diperbolehkan!")
            return
    else:
        print("Error: Operator tidak valid!")
        return

    # Menampilkan hasil
    print(f"Hasil: {hasil}")

# Memanggil fungsi
kalkulator()

Program kalkulator sederhana dalam Python adalah proyek yang baik untuk pemula dan programmer tingkat lanjut. Program ini memungkinkan pengguna untuk melakukan operasi matematika seperti penjumlahan, pengurangan, perkalian, dan pembagian.

 python
    angka1 = float(input("Masukkan angka pertama: "))
    angka2 = float(input("Masukkan angka kedua: "))
    operator = input("Masukkan operator (+, -, *, /): ").strip()


Pengguna diminta memasukkan angka pertama dan angka kedua, yang kemudian dikonversi menjadi tipe float agar bisa menerima bilangan desimal, Pengguna diminta memasukkan operator aritmatika, yaitu salah satu dari + (penjumlahan), - (pengurangan), * (perkalian), atau / (pembagian). Fungsi strip() digunakan untuk menghapus spasi yang mungkin tidak sengaja dimasukkan

python
if operator == "+":
        hasil = angka1 + angka2
    elif operator == "-":
        hasil = angka1 - angka2
    elif operator == "*":
        hasil = angka1 * angka2
    elif operator == "/":
        if angka2 != 0:
            hasil = angka1 / angka2
        else:
            print("Error: Pembagian dengan nol tidak diperbolehkan!")
            return


Jika operator adalah +, maka fungsi akan menjumlahkan kedua angka (angka1 + angka2), Jika operator adalah -, maka fungsi akan mengurangi angka pertama dengan angka kedua (angka1 - angka2), Jika operator adalah *, maka fungsi akan mengalikan angka pertama dengan angka kedua (angka1 * angka2), Jika operator adalah /, maka fungsi akan membagi angka pertama dengan angka kedua (angka1 / angka2). Namun, sebelum melakukan pembagian, fungsi memastikan bahwa angka kedua (angka2) tidak bernilai nol, karena pembagian dengan nol tidak valid dan akan menyebabkan error.

python
 else:
        print("Error: Operator tidak valid!")
        return

    # Menampilkan hasil
    print(f"Hasil: {hasil}")

# Memanggil fungsi
kalkulator()


Jika pengguna memasukkan operator yang tidak dikenali (bukan +, -, *, atau /), Setelah operasi berhasil dijalankan, hasil perhitungan akan ditampilkan kepada pengguna

Hasil program tersebut:

![gambar](https://github.com/user-attachments/assets/765d056b-f159-444a-b17b-920ef9e0e764)

Code program tersebut:

![gambar](https://github.com/user-attachments/assets/bff74048-f778-417d-9daf-2b4dd258a97c)

Dan ini flowchart nya :

![gambar](https://github.com/user-attachments/assets/a94f8685-4883-4999-9edf-e35817a985c6)



