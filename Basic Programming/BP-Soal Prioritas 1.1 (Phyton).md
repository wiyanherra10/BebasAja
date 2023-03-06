import math

# Fungsi untuk menghitung luas segitiga
def luas_segitiga(alas, tinggi):
    return 0.5 * alas * tinggi

# Fungsi untuk menghitung luas persegi panjang
def luas_persegi_panjang(panjang, lebar):
    return panjang * lebar

# Fungsi untuk menghitung luas lingkaran
def luas_lingkaran(jari_jari):
    return math.pi * jari_jari ** 2

# Main program
pilihan = input("Pilih bangun datar (segitiga/persegi panjang/lingkaran): ")

if pilihan == "segitiga":
    alas = float(input("Masukkan panjang alas: "))
    tinggi = float(input("Masukkan tinggi: "))
    print("Luas segitiga:", luas_segitiga(alas, tinggi))
elif pilihan == "persegi panjang":
    panjang = float(input("Masukkan panjang: "))
    lebar = float(input("Masukkan lebar: "))
    print("Luas persegi panjang:", luas_persegi_panjang(panjang, lebar))
elif pilihan == "lingkaran":
    jari_jari = float(input("Masukkan jari-jari: "))
    print("Luas lingkaran:", luas_lingkaran(jari_jari))
else:
    print("Pilihan tidak valid.")
