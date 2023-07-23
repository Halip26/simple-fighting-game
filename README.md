# Panduan Kode

Import Library

import random: Mengimport library random yang digunakan untuk menghasilkan angka random dalam permainan.

import tkinter: Mengimport library tkinter yang merupakan library GUI (Graphical User Interface) yang digunakan untuk membuat tampilan permainan.

Membuka File dan Membaca Nilai

wts = open("settings.txt", "r"): Membuka file "settings.txt" dalam mode membaca.

global fs: Mendeklarasikan variabel fs sebagai variabel global.

fs = int(wts.read()): Membaca isi file "settings.txt" dan mengubahnya menjadi tipe data integer kemudian disimpan dalam variabel fs.

print(fs): Mencetak nilai fs.

wts.close(): Menutup file "settings.txt".

Fungsi boxer(), kickboxer(), wrestler()

def boxer(): Mendefinisikan fungsi boxer yang akan dipanggil ketika tombol "Boxer" pada menu utama ditekan.

def kickboxer(): Mendefinisikan fungsi kickboxer yang akan dipanggil ketika tombol "Muay Thai" pada menu utama ditekan.

def wrestler(): Mendefinisikan fungsi wrestler yang akan dipanggil ketika tombol "Street Fighter" pada menu utama ditekan.

Fungsi menuGame()
def menuGame(): Mendefinisikan fungsi menuGame yang akan menampilkan tampilan menu utama permainan.
Fungsi togglefullscreen()
def togglefullscreen(): Mendefinisikan fungsi togglefullscreen yang akan mengatur mode fullscreen pada permainan.
Mendeklarasikan Variabel dan Membuat Tampilan Menu

title: Mendeklarasikan variabel title yang merupakan label judul permainan.

boxert, kickboxert, wrestlert: Mendeklarasikan variabel boxert, kickboxert, wrestlert yang merupakan tombol untuk memilih karakter.

mexit: Mendeklarasikan variabel mexit yang merupakan tombol untuk keluar dari permainan.

settings: Mendeklarasikan variabel settings yang merupakan label pengaturan permainan.

flscrn: Mendeklarasikan variabel flscrn yang merupakan label untuk mengaktifkan atau menonaktifkan mode fullscreen.

fsy: Mendeklarasikan variabel fsy yang merupakan tombol untuk mengaktifkan atau menonaktifkan mode fullscreen.

if fs == 0: ... elif fs == 1: ...: Mengatur mode fullscreen berdasarkan nilai fs yang telah dibaca dari file "settings.txt". Jika fs == 0, mode fullscreen dimatikan. Jika fs == 1, mode fullscreen diaktifkan.

```python
  if fs == 1:
            fs -= 1
            fsy.configure(text="Disabled")
            menu.attributes("-fullscreen", False)
            print("Fullscreen disabled")
            wts = open("settings.txt", "w")
            wts.write("0")
            wts.close()

        elif fs == 0:
            fs += 1
            fsy.configure(text="Enabled")
            menu.attributes("-fullscreen", True)
            print("Fullscreen enabled")
            wts = open("settings.txt", "w")
            wts.write("1")
            wts.close()
```

- Penjelasannya :
Kode ini adalah bagian dari fungsi togglefullscreen(). Fungsi ini digunakan untuk mengatur mode fullscreen pada permainan.

Pada bagian ini, pertama-tama dilakukan pengecekan apakah nilai variabel fs adalah 1 (fullscreen diaktifkan) atau 0 (fullscreen dimatikan).

Jika nilai fs == 1, maka dilakukan langkah-langkah berikut:

fs dikurangi 1 sehingga nilainya menjadi 0.
fsy (tombol untuk mengaktifkan/menonaktifkan fullscreen) diatur teksnya menjadi "Disabled".
Menu permainan (menu) diatur atribut "-fullscreen" menjadi False (mode fullscreen dimatikan).
Mencetak pesan "Fullscreen disabled".
File "settings.txt" dibuka dalam mode menulis.
Nilai "0" ditulis ke dalam file "settings.txt" (untuk menyimpan pengaturan fullscreen).
File "settings.txt" ditutup.

Jika nilai fs == 0, maka dilakukan langkah-langkah berikut:

fs ditambah 1 sehingga nilainya menjadi 1.
fsy diatur teksnya menjadi "Enabled".
Menu diatur atribut "-fullscreen" menjadi True (mode fullscreen diaktifkan).
Mencetak pesan "Fullscreen enabled".
File "settings.txt" dibuka dalam mode menulis.
Nilai "1" ditulis ke dalam file "settings.txt".
File "settings.txt" ditutup.

Dengan melakukan langkah-langkah di atas, fungsi togglefullscreen() akan mengubah pengaturan fullscreen permainan berdasarkan nilai fs.

mexit.pack(fill=tkinter.X, side=tkinter.BOTTOM): Menempatkan tombol mexit di bawah menu.

title.pack(): Menempatkan label title di menu.

boxert.pack(): Menempatkan tombol boxert di menu.

kickboxert.pack(): Menempatkan tombol kickboxert di menu.

wrestlert.pack(): Menempatkan tombol wrestlert di menu.

settings.pack(): Menempatkan label settings di menu.

flscrn.pack(): Menempatkan label flscrn di menu.
