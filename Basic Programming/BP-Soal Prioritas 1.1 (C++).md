#include <iostream>
#include <cmath>

using namespace std;

// Fungsi untuk menghitung luas segitiga
double luas_segitiga(double alas, double tinggi) {
    return 0.5 * alas * tinggi;
}

// Fungsi untuk menghitung luas persegi panjang
double luas_persegi_panjang(double panjang, double lebar) {
    return panjang * lebar;
}

// Fungsi untuk menghitung luas lingkaran
double luas_lingkaran(double jari_jari) {
    return M_PI * pow(jari_jari, 2);
}

int main() {
    string pilihan;
    double alas, tinggi, panjang, lebar, jari_jari;

    cout << "Pilih bangun datar (segitiga/persegi panjang/lingkaran): ";
    cin >> pilihan;

    if (pilihan == "segitiga") {
        cout << "Masukkan panjang alas: ";
        cin >> alas;
        cout << "Masukkan tinggi: ";
        cin >> tinggi;
        cout << "Luas segitiga: " << luas_segitiga(alas, tinggi) << endl;
    } else if (pilihan == "persegi panjang") {
        cout << "Masukkan panjang: ";
        cin >> panjang;
        cout << "Masukkan lebar: ";
        cin >> lebar;
        cout << "Luas persegi panjang: " << luas_persegi_panjang(panjang, lebar) << endl;
    } else if (pilihan == "lingkaran") {
        cout << "Masukkan jari-jari: ";
        cin >> jari_jari;
        cout << "Luas lingkaran: " << luas_lingkaran(jari_jari) << endl;
    } else {
        cout << "Pilihan tidak valid." << endl;
    }

    return 0;
}
