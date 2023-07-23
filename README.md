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

mexit.pack(fill=tkinter.X, side=tkinter.BOTTOM): Menempatkan tombol mexit di bawah menu.

title.pack(): Menempatkan label title di menu.

boxert.pack(): Menempatkan tombol boxert di menu.

kickboxert.pack(): Menempatkan tombol kickboxert di menu.

wrestlert.pack(): Menempatkan tombol wrestlert di menu.

settings.pack(): Menempatkan label settings di menu.

flscrn.pack(): Menempatkan label flscrn di menu.

fsy.pack(): Men
