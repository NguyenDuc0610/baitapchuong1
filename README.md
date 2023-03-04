import java.util.Scanner;

public class HonSo {
    private int nguyen; // phần nguyên
    private int tu; // tử số
    private int mau; // mẫu số

    // constructor không tham số
    public HonSo() {
        nguyen = 0;
        tu = 0;
        mau = 1;
    }

    // constructor có tham số
    public HonSo(int nguyen, int tu, int mau) {
        this.nguyen = nguyen;
        this.tu = tu;
        this.mau = mau;
    }

    // hàm nhập giá trị cho hỗn số
    public void nhapHonSo() {
        Scanner sc = new Scanner(System.in);
        System.out.print("Nhap phan nguyen: ");
        nguyen = sc.nextInt();
        System.out.print("Nhap tu so: ");
        tu = sc.nextInt();
        System.out.print("Nhap mau so: ");
        mau = sc.nextInt();
    }

    // hàm xuất giá trị của hỗn số
    public void xuatHonSo() {
        System.out.println(nguyen + " " + tu + "/" + mau);
    }
}
