public class Monomial {
    private double a; // Hệ số
    private int n; // Số mũ

    public Monomial() {
        this.a = 0;
        this.n = 0;
    }

    public Monomial(double a, int n) {
        this.a = a;
        this.n = n;
    }

    public void setA(double a) {
        this.a = a;
    }

    public void setN(int n) {
        this.n = n;
    }

    public double getA() {
        return a;
    }

    public int getN() {
        return n;
    }

    public void input() {
        Scanner sc = new Scanner(System.in);
        System.out.print("Nhap he so: ");
        this.a = sc.nextDouble();
        System.out.print("Nhap so mu: ");
        this.n = sc.nextInt();
    }

    public void output() {
        System.out.print(this.a + "x^" + this.n);
    }
}
