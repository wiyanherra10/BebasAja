def tambah(a, b):
    return a + b

def kurang(a, b):
    return a - b

def kali(a, b):
    return a * b

def bagi(a, b):
    return a / b

angka1 = float(input("Masukkan angka pertama: "))
angka2 = float(input("Masukkan angka kedua: "))
operator = input("Pilih operator (+, -, *, /): ")

hasil = 0

if operator == "+":
    hasil = tambah(angka1, angka2)
elif operator == "-":
    hasil = kurang(angka1, angka2)
elif operator == "*":
    hasil = kali(angka1, angka2)
elif operator == "/":
    hasil = bagi(angka1, angka2)
else:
    print("Operasi tidak dikenali")

print("Hasil: ", hasil)
