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


