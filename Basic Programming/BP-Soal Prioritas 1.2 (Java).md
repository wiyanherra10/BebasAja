import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Masukkan harga beli: ");
        int hargaBeli = scanner.nextInt();

        System.out.print("Masukkan harga jual: ");
        int hargaJual = scanner.nextInt();

        int untung = hargaJual - hargaBeli;
        if (untung > 0) {
            System.out.println("Untung sebesar: " + untung);
        } else if (untung < 0) {
            System.out.println("Rugi sebesar: " + Math.abs(untung));
        } else {
            System.out.println("Sama saja");
        }
    }
}
