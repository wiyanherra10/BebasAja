<?php
class Product {
  private $name;
  private $description;
  private $price;
  private $stock;

  public function setName($name) {
    $this->name = $name;
  }

  public function getName() {
    return $this->name;
  }

  public function setDescription($description) {
    $this->description = $description;
  }

  public function getDescription() {
    return $this->description;
  }

  public function setPrice($price) {
    $this->price = $price;
  }

  public function getPrice() {
    return $this->price;
  }

  public function setStock($stock) {
    $this->stock = $stock;
  }

  public function getStock() {
    return $this->stock;
  }

  public function getInfo() {
    echo "Product Name: ".$this->getName()."<br>";
    echo "Description: ".$this->getDescription()."<br>";
    echo "Price: ".$this->getPrice()."<br>";
    echo "Stock: ".$this->getStock()."<br>";
  }
}

// contoh penggunaan class Product
$produk1 = new Product();
$produk1->setName("Laptop Asus");
$produk1->setDescription("Laptop keren dengan spesifikasi tinggi");
$produk1->setPrice(10000000);
$produk1->setStock(10);
$produk1->getInfo();
?>
