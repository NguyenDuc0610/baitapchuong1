public class Point3D {
    private double x;
    private double y;
    private double z;

    public Point3D() {
        this.x = 0;
        this.y = 0;
        this.z = 0;
    }

    public Point3D(double x, double y, double z) {
        this.x = x;
        this.y = y;
        this.z = z;
    }

    public void setX(double x) {
        this.x = x;
    }

    public void setY(double y) {
        this.y = y;
    }

    public void setZ(double z) {
        this.z = z;
    }

    public double getX() {
        return x;
    }

    public double getY() {
        return y;
    }

    public double getZ() {
        return z;
    }

    public void input() {
        Scanner sc = new Scanner(System.in);
        System.out.print("Nhap toa do x: ");
        this.x = sc.nextDouble();
        System.out.print("Nhap toa do y: ");
        this.y = sc.nextDouble();
        System.out.print("Nhap toa do z: ");
        this.z = sc.nextDouble();
    }

    public void output() {
        System.out.println("(" + this.x + ", " + this.y + ", " + this.z + ")");
    }
}
