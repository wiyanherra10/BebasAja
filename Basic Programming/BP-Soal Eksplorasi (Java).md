import java.util.Scanner;

public class SimpleEncryption {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.print("Masukkan pesan yang akan dienkripsi: ");
        String message = input.nextLine().toUpperCase();

        String encryptedMessage = "";

        for (int i = 0; i < message.length(); i++) {
            char c = message.charAt(i);

            if (c >= 'A' && c <= 'Z') {
                int ascii = ((int) c) + 10;

                if (ascii > 'Z') {
                    ascii -= 26;
                }

                encryptedMessage += (char) ascii;
            } else {
                encryptedMessage += c;
            }
        }

        System.out.println("Pesan terenkripsi: " + encryptedMessage);
    }
}
