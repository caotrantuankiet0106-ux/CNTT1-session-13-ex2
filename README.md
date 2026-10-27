# 1. Cấu trúc cây thư mục dự án (greentech-system)
### Plaintext
greentech-system/
├── docs/
│   ├── README.md
│   └── srs-he-thong.docx
├── scripts/
│   └── auto_report.bat
├── data/
│   ├── log-he-thong.log
│   └── quan-ly-thiet-bi.xlsx
├── backup/
│   └── bao-cao-su-co.txt
└── .env
# 2. Nội dung tệp Shell Script (scripts/auto_report.bat)
### DOS
@echo off
echo ===== BAO CAO SU CO HE THONG ===== >> backup\bao-cao-su-co.txt
echo Thoi gian chay: %date% %time% >> backup\bao-cao-su-co.txt

type data\log-he-thong.log | findstr /I "CRITICAL ERROR TIMEOUT" >> backup\bao-cao-su-co.txt

echo Hoan tat loc log.
# 3. Nội dung tệp tài liệu (docs/README.md)
Markdown
## He thong quan tri ha tang GreenTech K26

### Cach chay script loc log
cd scripts
auto_report.bat

### Checklist kiem tra thiet bi
- [ ] Kiem tra ket noi tram cam bien
- [ ] Kiem tra dung luong RAM con trong
- [ ] Sao luu bao cao vao backup/

| Tram | RAM | Ngay lap dat |
|------|-----|--------------|
| tram-01 | 4GB | 2026-01-10 |
# 4. Công thức Excel (Đối soát tài nguyên)
Làm sạch mã linh kiện: =TRIM(A2)

Hàm VLOOKUP tra cứu thiết bị: =VLOOKUP(TRIM(B2), 'danh-muc-linh-kien'!$A$2:$D$100, 2, FALSE)

Hướng dẫn nộp: Bạn chỉ cần đẩy các tệp này lên GitHub (để chế độ Public) hoặc lưu vào Google Drive/Docs (bật quyền "Bất kỳ ai có link đều xem được"), sau đó copy đường dẫn dán vào ô nộp bài trên LMS là xong!
