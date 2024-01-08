# TugasUAS
### Made By Alfian Nur Rizki
### NIM 312310665

<h1>Buatlah program kasir di sebuah kantin, dengan kondisi berikut</h1>

+ <p>List opsi pilihan makanan/minuman dan aksi, bisa menggunakan format dictionary</p>
+ <p>Program harus meminta input pilihan makanan dari pengguna</p>
+ <p>Program harus menghitung total harga makanan yang dipesan</p>
+ <p>Program harus menampilkan struk pembelian </p>

<h1> Tampilan Program Kasir Kantin alzazali</h1>

![gambar](pict/uas.png)

<h1> Tampilan Output Program </h1>

![gambar](pict/outputuas.png)

<h1>Daftar Penggunaan Library Pada Program</h1>

## Input/Output (I/O):

+ <p>input() digunakan untuk menerima input dari pengguna melalui terminal.</p>
+ <p>print() digunakan untuk mencetak output ke terminal.</p>

## Struktur Data:

+ <p>dict (dictionary) digunakan untuk menyimpan data dalam bentuk kamus dengan kunci dan nilai.</p>
+ <p> list digunakan untuk menyimpan daftar pesanan dan detail pesanan.</p>

## Pengulangan dan Pengkondisian:

+ <p>while digunakan untuk membuat loop yang berjalan selama kondisinya benar.</p>
+ <p>if, elif, else digunakan untuk percabangan kondisi.</p>
+ <p>for digunakan untuk iterasi pada daftar menu.</p>

## String Formatting:

+ <p>format() digunakan untuk memformat string dengan menambahkan nilai ke dalam placeholder.</p>

<h1>Video Pembuatan Program Kasir</h1>

[Klik di sini untuk melihat pembuatan program](https://youtu.be/a_UsHIg2MTA)

<h1>Teks Program</h1>

```
harga_dict = {
    "Makanan": {
        "Nasi Goreng": 15000,
        "Ayam Goreng": 20000,
        "Bihun Goreng": 18000,
        "Pisang Goreng" : 8000,
    },
    "Minuman": {
        "Es Teh Manis": 7000,
        "Es Jeruk": 8000,
        "Kopi": 10000,
        "Boba Milktea" : 5000,
    },
}

menu_items = {
    "Makanan": ["Nasi Goreng", "Ayam Goreng", "Bihun Goreng","Pisang Goreng"],
    "Minuman": ["Es Teh Manis", "Es Jeruk", "Kopi","Boba Milktea"],
}

item_jumlah = {
    "Makanan": {"Nasi Goreng": 1, "Ayam Goreng": 2, "Bihun Goreng": 3, "Pisang Goreng": 4},
    "Minuman": {"Es Teh Manis": 1, "Es Jeruk": 2, "Kopi": 3, "Boba Milktea": 4},
}

order_details = []  # List untuk menyimpan detail pesanan

total_harga = 0

selesai = False

while True:
    print("Kantin Alzazali")
    print("Silahkan pilih makanan atau minuman:")
    print("1. Makanan")
    print("2. Minuman")

    pilih = input("Pilihan Anda: ")

    if pilih == "1":
        menu = "Makanan"
    elif pilih == "2":
        menu = "Minuman"
    else:
        print("Pilihan Anda tidak valid.")
        continue

    print("\nSilahkan pilih item:")

    for item in menu_items[menu]:
        print(f"{item_jumlah[menu][item]}. {item}")

    item_pilih = input("Pilihan Anda: ")
    item_pilih = int(item_pilih)

    for item in menu_items[menu]:
        if item_jumlah[menu][item] == item_pilih:
            harga = harga_dict[menu][item]
            total_harga += harga

            order_details.append((item, harga))  # Menambah detail pesanan ke list order_details

            print(f"\nAnda telah memesan {item} ({menu}).")
            print(f"Harga satuan: Rp {harga}")

            continue_order = input("Apakah Anda ingin memesan lagi? (y/n): ")
            if continue_order.lower() == "n":
                break
            else:
                break
    else:
        print("Pilihan Anda tidak valid.")

    transaction_end = input("Apakah transaksi telah selesai? (y/n): ")
    if transaction_end.lower() == "y":
        break

print("|====Struk Transaksi=====")
print("|========================")
print("|=====Detail Pesanan=====")
print("|========================")
print("|{:^11}|{:^11}|".format("menu", "harga"))
print("|========================")
for item, harga in order_details:
    print(f"| {item:<15} Rp {harga:>8,}")
print("|========================")
print(f"| Total harga:\tRp {total_harga}")
print("|========================")


```

### Kurang Lebihnya Mohon Maaf
### Karena Kesempurnaan Milik Allah Semata terima kasih
