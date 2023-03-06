#include <iostream>
#include <string>
using namespace std;

class Product {
  private:
    string name;
    string description;
    double price;
    int stock;

  public:
    void setName(string productName) {
      name = productName;
    }
    string getName() {
      return name;
    }

    void setDescription(string productDesc) {
      description = productDesc;
    }
    string getDescription() {
      return description;
    }

    void setPrice(double productPrice) {
      price = productPrice;
    }
    double getPrice() {
      return price;
    }

    void setStock(int productStock) {
      stock = productStock;
    }
    int getStock() {
      return stock;
    }

    void getInfo() {
      cout << "Product Name: " << name << endl;
      cout << "Description : " << description << endl;
      cout << "Price       : " << price << endl;
      cout << "Stock       : " << stock << endl;
    }
};

int main() {
  Product product1;

  product1.setName("Laptop");
  product1.setDescription("A high-performance laptop for gaming and work");
  product1.setPrice(1500.50);
  product1.setStock(10);

  product1.getInfo();

  return 0;
}
