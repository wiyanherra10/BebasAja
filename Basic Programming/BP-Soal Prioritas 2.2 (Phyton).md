n = int(input("Masukkan jumlah baris: "))

for i in range(n):
    for j in range(i+1):
        print("*", end="")
    print()
