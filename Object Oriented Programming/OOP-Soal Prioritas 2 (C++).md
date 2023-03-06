#include <iostream>
using namespace std;

// fungsi penjumlahan
double penjumlahan(double a, double b) {
    return a + b;
}

// fungsi pengurangan
double pengurangan(double a, double b) {
    return a - b;
}

// fungsi perkalian
double perkalian(double a, double b) {
    return a * b;
}

// fungsi pembagian
double pembagian(double a, double b) {
    return a / b;
}

int main() {
    double angka1, angka2;
    char operasi;

    cout << "Masukkan angka pertama: ";
    cin >> angka1;
    cout << "Masukkan angka kedua: ";
    cin >> angka2;
    cout << "Pilih operasi (+, -, *, /): ";
    cin >> operasi;

    switch (operasi) {
        case '+':
            cout << "Hasil penjumlahan: " << penjumlahan(angka1, angka2) << endl;
            break;
        case '-':
            cout << "Hasil pengurangan: " << pengurangan(angka1, angka2) << endl;
            break;
        case '*':
            cout << "Hasil perkalian: " << perkalian(angka1, angka2) << endl;
            break;
        case '/':
            if (angka2 == 0) {
                cout << "Pembagian dengan nol tidak terdefinisi" << endl;
            } else {
                cout << "Hasil pembagian: " << pembagian(angka1, angka2) << endl;
            }
            break;
        default:
            cout << "Operasi yang dimasukkan tidak valid" << endl;
            break;
    }

    return 0;
}
