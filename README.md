import java.util.Scanner;

public class Polynomial {
    private double[] coefficients; // Mảng lưu trữ các hệ số của đa thức

    public Polynomial(int degree) {
        this.coefficients = new double[degree + 1];
    }

    public Polynomial(double[] coefficients) {
        this.coefficients = coefficients;
    }

    public double[] getCoefficients() {
        return coefficients;
    }

    public void input() {
        Scanner sc = new Scanner(System.in);
        System.out.print("Nhap bac cua da thuc: ");
        int degree = sc.nextInt();
        this.coefficients = new double[degree + 1];
        for (int i = degree; i >= 0; i--) {
            System.out.print("Nhap he so cua x^" + i + ": ");
            this.coefficients[i] = sc.nextDouble();
        }
    }

    public void output() {
        int degree = coefficients.length - 1;
        for (int i = degree; i > 0; i--) {
            if (coefficients[i] != 0) {
                if (coefficients[i] == 1) {
                    System.out.print("x^" + i + " + ");
                } else if (coefficients[i] == -1) {
                    System.out.print("-x^" + i + " + ");
                } else {
                    System.out.print(coefficients[i] + "x^" + i + " + ");
                }
            }
        }
        if (coefficients[0] != 0) {
            System.out.print(coefficients[0]);
        } else if (degree == 0) {
            System.out.print("0");
        }
    }
}
