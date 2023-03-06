<?php
// Input harga beli dan harga jual
$hargaBeli = 15000;
$hargaJual = 30000;

// Hitung selisih harga jual dan beli
$selisihHarga = $hargaJual - $hargaBeli;

// Cek apakah mendapatkan keuntungan atau kerugian
if ($selisihHarga > 0) {
    echo "Untung sebesar: " . $selisihHarga;
} else if ($selisihHarga < 0) {
    echo "Rugi sebesar: " . abs($selisihHarga);
} else {
    echo "Sama saja";
}
?>
