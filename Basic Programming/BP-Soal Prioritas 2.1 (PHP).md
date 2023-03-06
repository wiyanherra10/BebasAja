function drawXYZ($height) {
    for ($i = 1; $i <= $height; $i++) {
        if ($i % 3 == 0) {
            echo "X";
        } else if ($i % 2 == 1) {
            echo "Y";
        } else {
            echo "Z";
        }
    }
}
