#include <stdio.h>

typedef struct {
    char tenMatHang[21];    // Tên mặt hàng (tối đa 20 ký tự)
    int donGia;             // Đơn giá
    int soLuongTon;         // Số lượng tồn
} MATHANG;

// Hàm nhập thông tin một mặt hàng
void nhapMatHang(MATHANG *mh) {
    printf("Nhap ten mat hang: ");
    fgets(mh->tenMatHang, 21, stdin);
    printf("Nhap don gia: ");
    scanf("%d", &mh->donGia);
    printf("Nhap so luong ton: ");
    scanf("%d", &mh->soLuongTon);
}

// Hàm xuất thông tin một mặt hàng
void xuatMatHang(const MATHANG *mh) {
    printf("%-20s%10d VND   So luong ton: %d\n", mh->tenMatHang, mh->donGia, mh->soLuongTon);
}

int main() {
    MATHANG mh;
    nhapMatHang(&mh);
    xuatMatHang(&mh);
    return 0;
}
