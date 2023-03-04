public class Point {
    private double x;
    private double y;

    public Point() {
        this.x = 0;
        this.y = 0;
    }

    public Point(double x, double y) {
        this.x = x;
        this.y = y;
    }

    public void setX(double x) {
        this.x = x;
    }

    public void setY(double y) {
        this.y = y;
    }

    public double getX() {
        return x;
    }

    public double getY() {
        return y;
    }

    public void input() {
        Scanner sc = new Scanner(System.in);
        System.out.print("Nhap toa do x: ");
        this.x = sc.nextDouble();
        System.out.print("Nhap toa do y: ");
        this.y = sc.nextDouble();
    }

    public void output() {
        System.out.println("(" + this.x + ", " + this.y + ")");
    }
}
