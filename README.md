typedef struct {
    char maCauThu[11];
    char tenCauThu[31];
    NGAY ngaySinh;
} CAUTHU;

void nhapCauThu(CAUTHU *ct) {
    printf("Nhap ma cau thu: ");
    fflush(stdin);
    gets(ct->maCauThu);
    printf("Nhap ten cau thu: ");
    fflush(stdin);
    gets(ct->tenCauThu);
    printf("Nhap ngay sinh: \n");
    nhapNgay(&ct->ngaySinh);
}

void xuatCauThu(CAUTHU ct) {
    printf("Ma cau thu: %s\n", ct.maCauThu);
    printf("Ten cau thu: %s\n", ct.tenCauThu);
    printf("Ngay sinh: ");
    xuatNgay(ct.ngaySinh);
}
