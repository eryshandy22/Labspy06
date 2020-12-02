# Labspy06
**Nama	   	: Ery Shandy** <br>
**Nim	  	  : 312010201** <br>
**Kelas	  	: TI.20.A2** <br>
**Matkul	  : Bahasa Pemrograman** <br>
# Praktikum 6
## Latihan
<img width="291" alt="latihan" src="https://user-images.githubusercontent.com/73053784/100827099-85386c80-348e-11eb-8a14-057948b8d125.png">

## Hasil Source Code Diatas
```python
#Ery Shandy
print("________________________________________")
#mengubah function menggunakan lambda
def a(x):
    return x ** 2

lambda x: x ** 2

print("1. Mengubah function menggunakan Lambda \n   def a(x): \n \t   return x ** 2")
print("   Hasil : lambda x: x ** 2")

def b(x, y):
    return math.sqrt(x ** 2 + y ** 2)

lambda x, y: math.sqrt(x ** 2 + y ** 2)

print("________________________________________")
print("2. Mengubah function menggunakan Lambda \n   def b(x, y): \n \t   return math.sqrt(x ** 2 + y ** 2)")
print("   Hasil : lambda x, y: math.sqrt(x ** 2 + y ** 2))")

def c(*args):
    return sum(args) / len(args)

lambda *args: sum(args) / len(args)

print("________________________________________")
print("3. Mengubah function menggunakan Lambda \n   def c(*args): \n \t   return sum(args) / len(args)")
print("   Hasil : lambda *args: sum(args) / len(args))")

def d(s):
    return "".join(set(s))

lambda s: "".join(set(s))

print("________________________________________")
print("4. Mengubah function menggunakan Lambda \n   def d(s): \n \t   return "".join(set(s))")
print("   Hasil : lambda s: "".join(set(s)))")
```

Disini saya sudah rubah ke lambda Kalau di Tugas Latihan tidak ada outputnya, tapi disini saya akan berikan contoh untuk output dari source code tersebut Berikut outputnya
<img width="899" alt="ss latihan" src="https://user-images.githubusercontent.com/73053784/100827579-a51c6000-348f-11eb-90ab-da992bdf1e62.png">

Dalam Hasil INPUTAN Diatas Ialah hasil dari proses lambda

## Tugas Praktikum
<img width="280" alt="praktikum" src="https://user-images.githubusercontent.com/73053784/100827730-02181600-3490-11eb-90df-be541b2fb339.png">

## Hasil Source Code Diatas
```python
#Ery Shandy
data = {}

def tambah():
    print("Tambah Data")
    nama = input("Nama\t\t: ")
    nim = int(input("NIM\t\t\t: "))
    tugas = int(input("NIlai Tugas\t: "))
    uts = int(input("Nilai UTS\t: "))
    uas = int(input("Nilai UAS\t: "))
    nilaiakhir = (tugas * 0.3 + uts * 0.35 + uas * 0.35)
    data[nama] = nim, tugas, uts, uas, nilaiakhir


def tampilkan():
    if data.items():
        print("~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~| Daftar Nilai |~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~")
        print("_______________________________________________________________________________________")
        print("|  No  |      NIM      |      NAMA         |    TUGAS   |   UTS   |   UAS   | AKHIR  |")
        print("|______|_______________|___________________|____________|_________|_________|________|__")
        i = 0
        for a in data.items():
            i += 1
            print(f"| {i:4} | {a[0]:13s} | {a[1][0]:17} | {a[1][1]:10d} |  {a[1][2]:6d} | {a[1][2]:7d} | {a[1][4]:6.2f} | ")
    else:
        print("~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~| Daftar Nilai |~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~")
        print("_______________________________________________________________________________________")
        print("|  No  |      Nama     |      NIM      |   TUGAS  |   UTS   |   UAS   | Nilai Akhir  |")
        print("_______________________________________________________________________________________")
        print("|      |               |             Tidak Ada Data         |         |                |")
    print("____________________________________________________________________________________________")


def hapus():
    print("Hapus Data Nilai Mahasiswa")
    nama = input(" Masukan Nama\t:")
    if nama in data.keys():
        del data[nama]
        print()
        print("~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~")
        print("===| BERHASIL MENGHAPUS DATA |===")
        print("~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~")
    else:
        print("Data {0} tidak ada".format(nama))


def ubah():
    print("~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~")
    print("===| Edit Data Nilai Mahasiswa |===")
    print("~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~")
    nama = input("Masukan Nama\t\t: ")
    print("___________________________________")
    if nama in data.keys():
        nim = input("NIM baru\t\t\t: ")
        tugas = int(input("Nilai Tugas Baru\t: "))
        uts = int(input("Nilai UTS Baru\t\t: "))
        uas = int(input("Nilai UAS Baru\t\t: "))
        nilaiakhir = (tugas * 30 / 100 + uts * 35 / 100 + uas * 35 / 100)
        data[nama] = nim, tugas, uts, uas, nilaiakhir
        print()
        print("<><><><><><><><><><><><><><><><>")
        print("====| BERHASIL MENGUBAH DATA |====")
        print("<><><><><><><><><><><><><><><><>")
    else:
        print("Data nilai {0} tidak ada ".format(nama))


while True:
    print("")
    print("|_<><><><><><><><><><><><><><><><><>_|")
    print("|~~~~~~~~| DATA MAHASISWA |~~~~~~~~~~|")
    print("|_<><><><><><><><><><><><><><><><><>_|")
    x = input("1.| Lihat Data \n2.| Tambah Data \n3.| Ubah Data \n4.| Hapus Data \n0.| Keluar Aplikasi \nPilih menu : ")
    if x.lower() == "1":
        tampilkan()
    elif x.lower() == "2":
        tambah()
    elif x.lower() == "3":
        ubah()
    elif x.lower() == "4":
        hapus()
    elif x.lower() == "0":
        print()
        print("<><><><><><><><><><><><><><><><>")
        print("====== KELUAR DARI PROGRAM ======")
        print("<><><><><><><><><><><><><><><><>")
        break

    else:
        print()
        print("<><><><><><><><><><><><><><><><>")
        print("== Pilihan Anda Tidak Tersedia ==")
        print("== Pilihlah Menu Yang Tersedia ==")
        print("<><><><><><><><><><><><><><><><>")
 ```
 
 * Pada tugas praktikum saya menggunakan fitur function yang ada di Python. Dan menggunakan media penyimpanan data berupa Dictionary
Saya akan menjelaskan dikit mengenai fitur-fitur yang ada dalam program sederhana saya.
Ketika program di run pada pertama kali, maka akan muncul tampilan seperti ini :
<img width="879" alt="ss praktikum" src="https://user-images.githubusercontent.com/73053784/100828230-3dffab00-3491-11eb-8c1a-42801ae0e484.png">

 Terdapat 5 Pilihan menu, yaitu :

   1 Tambah Data
   2 Lihat Data
   3 Ubah Data
   4 Hapus Data
   0 Keluar Aplikasi
   
* Menambahkan Data <br>
<img width="897" alt="praktikum 1" src="https://user-images.githubusercontent.com/73053784/100829441-f0d10880-3493-11eb-9c22-afd0235f4835.png">


* Lihat Data Nilai Mahasiswa<br>
System akan menjalankan fitur ini ketika user mengetikkan perintah 2 pada pilihan Pilih Menu (1-2-3-4-5)
Inilah tampilan fitur Lihat Data :
<img width="877" alt="praktikum 3" src="https://user-images.githubusercontent.com/73053784/100829391-d565fd80-3493-11eb-9ee0-ec2166d9ec4c.png">

* ubah data <br> 
Pada fitur ini user akan diminta untuk memilih data siapa yang akan diubah dan data apa yang akan dirubah
Setelah user memilih data, Misalnya user ingin merubah NIM dari mahasiswa dengan nama rizky , Maka akan muncul tampilan seperti ini :
<img width="875" alt="praktikum 4" src="https://user-images.githubusercontent.com/73053784/100829776-c16ecb80-3494-11eb-9ad5-035617ca6640.png">

* Fitur Hapus Data Nilai Mahasiswa <br>
System akan menjalankan fitur ini ketika user mengetikkan perintah 4 pada pilihan Pilih Menu (1-2-3-4-5)
Sebelum saya menjalankan fitur ini, saya akan menambahkan 1 data lagi dengan nama Ery
<img width="878" alt="praktikum 2" src="https://user-images.githubusercontent.com/73053784/100829899-0561d080-3495-11eb-9059-f57c9b758d71.png">

# Flowchart
<img width="324" alt="flowchart" src="https://user-images.githubusercontent.com/73053784/100829995-478b1200-3495-11eb-9e15-c6c3cf90954c.png">




