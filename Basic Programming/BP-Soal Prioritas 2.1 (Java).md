public class DrawXYZ {
    public static void draw(int height) {
        for (int i = 1; i <= height; i++) {
            if (i % 3 == 0) {
                System.out.print("X");
            } else if (i % 2 == 1) {
                System.out.print("Y");
            } else {
                System.out.print("Z");
            }
        }
    }

    public static void main(String[] args) {
        int height = 10;
        draw(height);
    }
}
