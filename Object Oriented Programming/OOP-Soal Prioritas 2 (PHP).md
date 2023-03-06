<?php

function tambah($a, $b)
{
    return $a + $b;
}

function kurang($a, $b)
{
    return $a - $b;
}

function kali($a, $b)
{
    return $a * $b;
}

function bagi($a, $b)
{
    return $a / $b;
}

// Fungsi utama
if ($_SERVER["REQUEST_METHOD"] == "POST") {
    $angka1 = $_POST["angka1"];
    $angka2 = $_POST["angka2"];
    $operator = $_POST["operator"];

    switch ($operator) {
        case "+":
            $hasil = tambah($angka1, $angka2);
            break;
        case "-":
            $hasil = kurang($angka1, $angka2);
            break;
        case "*":
            $hasil = kali($angka1, $angka2);
            break;
        case "/":
            $hasil = bagi($angka1, $angka2);
            break;
        default:
            $hasil = "Operasi tidak dikenali";
    }
}
?>

<!DOCTYPE html>
<html>

<head>
    <title>Kalkulator Sederhana</title>
</head>

<body>
    <h1>Kalkulator Sederhana</h1>
    <form method="post" action="<?php echo htmlspecialchars($_SERVER["PHP_SELF"]); ?>">
        <label for="angka1">Angka 1:</label>
        <input type="number" id="angka1" name="angka1" required><br><br>

        <label for="angka2">Angka 2:</label>
        <input type="number" id="angka2" name="angka2" required><br><br>

        <label for="operator">Operator:</label>
        <select id="operator" name="operator">
            <option value="+">+</option>
            <option value="-">-</option>
            <option value="*">*</option>
            <option value="/">/</option>
        </select><br><br>

        <input type="submit" value="Hitung">
    </form>

    <?php
    if (isset($hasil)) {
        echo "<h2>Hasil:</h2>";
        echo $angka1 . " " . $operator . " " . $angka2 . " = " . $hasil;
    }
    ?>
</body>

</html>
