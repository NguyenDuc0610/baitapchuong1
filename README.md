#include <stdio.h>

typedef struct {
    char nhanHieu[21]; // Nhãn hiệu (tối đa 20 ký tự)
    double trongLuong; // Trọng lượng
    struct {
        int ngay;
        int thang;
        int nam;
    } hanSuDung;        // Hạn sử dụng (kiểu dữ liệu NGAY)
} HOPSUA;

// Hàm nhập thông tin một hộp sữa
void nhapHopsua(HOPSUA *hs) {
    printf("Nhap nhan hieu: ");
    fgets(hs->nhanHieu, 21, stdin);
    printf("Nhap trong luong: ");
    scanf("%lf", &hs->trongLuong);
    printf("Nhap han su dung (ngay thang nam): ");
    scanf("%d%d%d", &hs->hanSuDung.ngay, &hs->hanSuDung.thang, &hs->hanSuDung.nam);
}

// Hàm xuất thông tin một hộp sữa
void xuatHopsua(const HOPSUA *hs) {
    printf("%-20s%10.2lf   Han su dung: %02d/%02d/%04d\n", hs->nhanHieu,
           hs->trongLuong, hs->hanSuDung.ngay, hs->hanSuDung.thang, hs->hanSuDung.nam);
}

int main() {
    HOPSUA hs;
    nhapHopsua(&hs);
    xuatHopsua(&hs);
    return 0;
}
