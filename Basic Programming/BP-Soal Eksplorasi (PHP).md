<?php
function enkripsi($text)
{
  $result = "";
  $length = strlen($text);
  $shift = 10;
  for($i=0; $i<$length; $i++)
  {
    if (ctype_alpha($text[$i]))
    {
      $ascii = ord($text[$i]);
      $shifted_ascii = $ascii + $shift;
      if (ctype_upper($text[$i]))
      {
        if ($shifted_ascii > ord('Z'))
        {
          $shifted_ascii -= 26;
        }
      }
      else
      {
        if ($shifted_ascii > ord('z'))
        {
          $shifted_ascii -= 26;
        }
      }
      $result .= chr($shifted_ascii);
    }
    else
    {
      $result .= $text[$i];
    }
  }
  return $result;
}

// Contoh penggunaan
$text = "Ini adalah contoh enkripsi sederhana dengan pergeseran 10 urutan alphabet.";
echo "Text asli: " . $text . "\n";
$text_enkripsi = enkripsi($text);
echo "Text terenkripsi: " . $text_enkripsi . "\n";
?>
