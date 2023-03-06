#include <stdio.h>

typedef struct {
    char tenPhim[21];       // Tên phim (tối đa 20 ký tự)
    int giaTien;            // Giá tiền
    struct {
        int gio;
        int phut;
    } xuatChieu;            // Xuất chiếu (kiểu dữ liệu THOIGIAN)
    struct {
        int ngay;
        int thang;
        int nam;
    } ngayXem;              // Ngày xem (kiểu dữ liệu NGAY)
} VE;

// Hàm nhập thông tin một vé xem phim
void nhapVe(VE *v) {
    printf("Nhap ten phim: ");
    fgets(v->tenPhim, 21, stdin);
    printf("Nhap gia tien: ");
    scanf("%d", &v->giaTien);
    printf("Nhap gio xuat chieu (gio phut): ");
    scanf("%d%d", &v->xuatChieu.gio, &v->xuatChieu.phut);
    printf("Nhap ngay xem (ngay thang nam): ");
    scanf("%d%d%d", &v->ngayXem.ngay, &v->ngayXem.thang, &v->ngayXem.nam);
}

// Hàm xuất thông tin một vé xem phim
void xuatVe(const VE *v) {
    printf("%-20s%10d VND   Xuat chieu: %02d:%02d   Ngay xem: %02d/%02d/%04d\n", v->tenPhim,
           v->giaTien, v->xuatChieu.gio, v->xuatChieu.phut, v->ngayXem.ngay, v->ngayXem.thang, v->ngayXem.nam);
}

int main() {
    VE v;
    nhapVe(&v);
    xuatVe(&v);
    return 0;
}
