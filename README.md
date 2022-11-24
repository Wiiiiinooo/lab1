# lab1
import java.util.Arrays;
class Main {
    public static void main(String[] args) {
        int[] a = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16};
        System.out.println(Arrays.toString(a));
        float[] x = new float[16];
        for (int i = 0; i < x.length; i++) {
            x[i] = ((float) (Math.random() * 28.0f) - 15.0f);
            System.out.println(x[i] + " ");
        }
        double[][] b = new double[16][16];
        for (int i = 0; i < 16; i++) {
            for (int j = 0; j < 16; j++) {
                if (a[i] == 16) {
                    b[i][j] = Math.asin(Math.exp(Math.cbrt(Math.pow(-Math.cos(x[j]), 2))));
                }
                if (a[i] == 4 || a[i] == 5 || a[i] == 7 || a[i] == 11 || a[i] == 12 || a[i] == 13 || a[i] == 14 || a[i] == 15) {
                    b[i][j]=Math.sin(Math.tan(x[j]));
                } else {
                    b[i][j] = 2*Math.tan(Math.pow(Math.pow((x[j]+2/3),x[j])/3,Math.cos(x[j])));
                }
            }
        }
        for (int i = 0; i < 16; i++) {
            for (int j = 0; j < 16; j++){
                System.out.printf("%10.3f",b[i][j]);

            }
            System.out.println( );
        }

    }
}
