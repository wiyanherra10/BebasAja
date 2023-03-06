<?php
// Fungsi untuk menghitung luas segitiga
function luasSegitiga($alas, $tinggi) {
    return 0.5 * $alas * $tinggi;
}

// Fungsi untuk menghitung luas persegi panjang
function luasPersegiPanjang($panjang, $lebar) {
    return $panjang * $lebar;
}

// Fungsi untuk menghitung luas lingkaran
function luasLingkaran($jari_jari) {
    return pi() * pow($jari_jari, 2);
}

// Ambil input dari pengguna
$pilihan = $_POST["pilihan"];

// Jika pilihan adalah "segitiga"
if ($pilihan == "segitiga") {
    $alas = $_POST["alas"];
    $tinggi = $_POST["tinggi"];
    $luas = luasSegitiga($alas, $tinggi);
    echo "Luas segitiga: $luas";
} 
// Jika pilihan adalah "persegi panjang"
else if ($pilihan == "persegi panjang") {
    $panjang = $_POST["panjang"];
    $lebar = $_POST["lebar"];
    $luas = luasPersegiPanjang($panjang, $lebar);
    echo "Luas persegi panjang: $luas";
}
// Jika pilihan adalah "lingkaran"
else if ($pilihan == "lingkaran") {
    $jari_jari = $_POST["jari-jari"];
    $luas = luasLingkaran($jari_jari);
    echo "Luas lingkaran: $luas";
}
// Jika pilihan tidak valid
else {
    echo "Pilihan tidak valid.";
}
?>
