harga_beli = float(input("Masukkan harga beli: "))
harga_jual = float(input("Masukkan harga jual: "))

if harga_jual > harga_beli:
    keuntungan = harga_jual - harga_beli
    print("Anda untung sebesar: ", keuntungan)
elif harga_jual < harga_beli:
    kerugian = harga_beli - harga_jual
    print("Anda rugi sebesar: ", kerugian)
else:
    print("Sama saja")
