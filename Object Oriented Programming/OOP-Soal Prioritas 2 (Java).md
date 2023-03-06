import java.util.Scanner;

public class Kalkulator {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Masukkan angka pertama: ");
        double angka1 = scanner.nextDouble();

        System.out.print("Masukkan angka kedua: ");
        double angka2 = scanner.nextDouble();

        System.out.print("Pilih operator (+, -, *, /): ");
        String operator = scanner.next();

        double hasil = 0;

        switch (operator) {
            case "+":
                hasil = tambah(angka1, angka2);
                break;
            case "-":
                hasil = kurang(angka1, angka2);
                break;
            case "*":
                hasil = kali(angka1, angka2);
                break;
            case "/":
                hasil = bagi(angka1, angka2);
                break;
            default:
                System.out.println("Operasi tidak dikenali");
        }

        System.out.println("Hasil: " + hasil);

        scanner.close();
    }

    public static double tambah(double a, double b) {
        return a + b;
    }

    public static double kurang(double a, double b) {
        return a - b;
    }

    public static double kali(double a, double b) {
        return a * b;
    }

    public static double bagi(double a, double b) {
        return a / b;
    }
}
