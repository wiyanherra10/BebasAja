public class Product {
    private String name;
    private String description;
    private double price;
    private int stock;

    public void setName(String name) {
        this.name = name;
    }

    public String getName() {
        return name;
    }

    public void setDescription(String description) {
        this.description = description;
    }

    public String getDescription() {
        return description;
    }

    public void setPrice(double price) {
        this.price = price;
    }

    public double getPrice() {
        return price;
    }

    public void setStock(int stock) {
        this.stock = stock;
    }

    public int getStock() {
        return stock;
    }

    public void getInfo() {
        System.out.println("Product Name: " + name);
        System.out.println("Product Description: " + description);
        System.out.println("Product Price: " + price);
        System.out.println("Product Stock: " + stock);
    }
}
