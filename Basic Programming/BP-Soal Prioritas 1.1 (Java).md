import java.util.Scanner;

public class LuasBangunDatar {
    // Fungsi untuk menghitung luas segitiga
    public static double luasSegitiga(double alas, double tinggi) {
        return 0.5 * alas * tinggi;
    }

    // Fungsi untuk menghitung luas persegi panjang
    public static double luasPersegiPanjang(double panjang, double lebar) {
        return panjang * lebar;
    }

    // Fungsi untuk menghitung luas lingkaran
    public static double luasLingkaran(double jari_jari) {
        return Math.PI * Math.pow(jari_jari, 2);
    }

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        String pilihan;
        double alas, tinggi, panjang, lebar, jari_jari;

        System.out.print("Pilih bangun datar (segitiga/persegi panjang/lingkaran): ");
        pilihan = input.nextLine();

        if (pilihan.equals("segitiga")) {
            System.out.print("Masukkan panjang alas: ");
            alas = input.nextDouble();
            System.out.print("Masukkan tinggi: ");
            tinggi = input.nextDouble();
            System.out.println("Luas segitiga: " + luasSegitiga(alas, tinggi));
        } else if (pilihan.equals("persegi panjang")) {
            System.out.print("Masukkan panjang: ");
            panjang = input.nextDouble();
            System.out.print("Masukkan lebar: ");
            lebar = input.nextDouble();
            System.out.println("Luas persegi panjang: " + luasPersegiPanjang(panjang, lebar));
        } else if (pilihan.equals("lingkaran")) {
            System.out.print("Masukkan jari-jari: ");
            jari_jari = input.nextDouble();
            System.out.println("Luas lingkaran: " + luasLingkaran(jari_jari));
        } else {
            System.out.println("Pilihan tidak valid.");
        }
    }
}
