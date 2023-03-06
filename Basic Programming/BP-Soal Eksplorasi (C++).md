#include <iostream>
#include <string>
using namespace std;

string encrypt(string input){
    string output = "";
    int length = input.length();
    for(int i=0; i<length; i++){
        if(input[i] >= 'A' && input[i] <= 'Z'){
            output += (input[i] + 10 - 'A') % 26 + 'A';  // pergeseran 10 urutan alphabet
        }
        else{
            output += input[i];  // karakter selain alphabet tidak dienkripsi
        }
    }
    return output;
}

int main(){
    string input;
    cout << "Masukkan teks yang akan dienkripsi: ";
    getline(cin, input);
    string encrypted = encrypt(input);
    cout << "Hasil enkripsi: " << encrypted << endl;
    return 0;
}
