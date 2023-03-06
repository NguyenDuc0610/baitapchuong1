#include <stdio.h>

typedef struct {
    char maChuyenBay[6];    // Mã chuyến bay (tối đa 5 ký tự)
    char noiDi[21];         // Nơi đi (tối đa 20 ký tự)
    char noiDen[21];        // Nơi đến (tối đa 20 ký tự)
    NGAY ngayBay;           // Ngày bay
    THOIGIAN gioBay;        // Giờ bay
} CHUYENBAY;

// Hàm nhập thông tin một chuyến bay
void nhapChuyenBay(CHUYENBAY *cb) {
    printf("Nhap ma chuyen bay: ");
    fgets(cb->maChuyenBay, 6, stdin);
    printf("Nhap noi di: ");
    fgets(cb->noiDi, 21, stdin);
    printf("Nhap noi den: ");
    fgets(cb->noiDen, 21, stdin);
    printf("Nhap ngay bay (ngay/thang/nam): ");
    nhapNgay(&cb->ngayBay);
    printf("Nhap gio bay (gio:phut): ");
    nhapThoiGian(&cb->gioBay);
}

// Hàm xuất thông tin một chuyến bay
void xuatChuyenBay(const CHUYENBAY *cb) {
    printf("Ma chuyen bay: %s\n", cb->maChuyenBay);
    printf("Noi di: %s", cb->noiDi);
    printf("Noi den: %s", cb->noiDen);
    printf("Ngay bay: ");
    xuatNgay(&cb->ngayBay);
    printf("Gio bay: ");
    xuatThoiGian(&cb->gioBay);
}

int main() {
    CHUYENBAY cb;
    nhapChuyenBay(&cb);
    xuatChuyenBay(&cb);
    return 0;
}
