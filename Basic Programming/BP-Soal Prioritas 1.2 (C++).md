#include <iostream>
using namespace std;

int main() {
    // Input harga beli dan harga jual
    int hargaBeli, hargaJual;
    cout << "Masukkan harga beli: ";
    cin >> hargaBeli;
    cout << "Masukkan harga jual: ";
    cin >> hargaJual;

    // Hitung selisih harga jual dan beli
    int selisihHarga = hargaJual - hargaBeli;

    // Cek apakah mendapatkan keuntungan atau kerugian
    if (selisihHarga > 0) {
        cout << "Untung sebesar: " << selisihHarga;
    } else if (selisihHarga < 0) {
        cout << "Rugi sebesar: " << abs(selisihHarga);
    } else {
        cout << "Sama saja";
    }

    return 0;
}
