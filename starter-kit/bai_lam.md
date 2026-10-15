# BÀI LÀM – HACKATHON 01

  

-  **Mã đề:** 03

-  **Họ tên:** Nguyễn Trần Anh Dũng

-  **Lớp:** CNTT4

-  **Link repository:**https://github.com/dungxnguyen2007-max/HN-KS26-CNTT4_Nhap-mon-CNTT_Hackathon03-

-  **Hệ điều hành (Windows/macOS):**Windows

  

## 4.2. Thao tác máy tính cơ bản bằng CLI

  

### Các lệnh đã chạy

  

```powershell

# Ghi lần lượt các lệnh đã chạy, mỗi lệnh một dòng
pwd
ls -Force
mv .\lich_tap.txt .\docs\
mv .\logo_phong_gym.PNG .\media\
cp .\media\logo_phong_gym.PNG .\backup\
rm .\temp_103.tmp
cd .\logs\
ls -Force
cd ..

```

  

### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

  

```text

    Directory: C:\starter-kit\gym-website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        10/15/2026   8:07 AM                backup
d-----        10/15/2026   8:02 AM                data
d-----        10/15/2026   8:06 AM                docs
d-----        10/15/2026   8:02 AM                logs
d-----        10/15/2026   8:06 AM                media
-a----        10/15/2026   7:55 AM             68 .env


    Directory: C:\starter-kit\gym-website\backup


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/15/2026   7:55 AM           6194 logo_phong_gym.PNG


    Directory: C:\starter-kit\gym-website\data


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/15/2026   7:55 AM           6089 dang_ky_thang_11.xlsx


    Directory: C:\starter-kit\gym-website\docs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/15/2026   7:55 AM             75 lich_tap.txt


    Directory: C:\starter-kit\gym-website\logs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/15/2026   7:55 AM           1085 member.log


    Directory: C:\starter-kit\gym-website\media


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/15/2026   7:55 AM           6194 logo_phong_gym.PNG


  

```

  

## 4.3. Lọc log thủ công

  

### Lệnh đã chạy

  

```powershell

Get-Content .\logs\member.log | select-string "ERROR"
Get-Content .\logs\member.log | select-string "ERROR" > logs/daily_report.txt

  

```

  

### 2 dòng lỗi đầu tiên trong daily_report.txt

  

```text

2025-11-28 07:26:18 [ERROR] Khong tim thay trang /lich-tap (404)
2025-11-28 07:29:18 [ERROR] Het thoi gian cho (timeout)

  

```

  

## 4.4. Thao tác với tài liệu Markdown (README.md)

  

> README.md được chấm trực tiếp trên file `README.md` ở gốc dự án. Đánh dấu `[x]` vào các mục đã làm để tự kiểm tra.

  

- [x] Heading 1: tên dự án

- [x] Mô tả ngắn có cả **in đậm** và *in nghiêng*

- [X] Bảng `Thư mục | Nội dung`, ít nhất 3 dòng dữ liệu

- [X] Code block chứa lệnh PowerShell/Terminal liệt kê nội dung dự án

- [X] Task list ít nhất 2 công việc, có ít nhất 1 mục đã hoàn thành

- [X] Blockquote nhắc không upload `.env`

  

## 4.5. Chạy script auto_report (.ps1 hoặc .sh)

  

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

  

```shell

.\auto_report.ps1

  

```

  

### Kết quả hiển thị

  

```text

Dang loc log...
Hoan thanh!

  

```

  

## 4.6. Đếm số dòng lỗi

  

### Lệnh

  

```shell

(Get-Content logs/member.log | Select-String "ERROR").count

  

```

  

### Kết quả đếm (Windows: giá trị Count; macOS: con số in ra)

  

```text

7

  

```

  

## 4.7. Báo cáo tổng hợp

  

### Các lệnh đã chạy

  

```powershell

ni logs/tong_hop.txt
"=== TONG HOP LOG ===" > .\logs\tong_hop.txt
select-string "WARNING" logs/member.log >> .\logs\tong_hop.txT
select-string "ERROR" logs/member.log >> .\logs\tong_hop.txT

  

```

  

### Nội dung file logs/tong_hop.txt

  

```text

=== TONG HOP LOG ===

logs\member.log:3:2025-11-28 07:14:18 [WARNING] Phong tap dong nguoi
logs\member.log:17:2025-11-28 07:56:18 [WARNING] Phong tap dong nguoi
logs\member.log:18:2025-11-28 07:59:18 [WARNING] The tu sap het han



logs\member.log:7:2025-11-28 07:26:18 [ERROR] Khong tim thay trang /lich-tap (404)
logs\member.log:8:2025-11-28 07:29:18 [ERROR] Het thoi gian cho (timeout)
logs\member.log:9:2025-11-28 07:32:18 [ERROR] Khong tim thay trang /lich-tap (404)
logs\member.log:10:2025-11-28 07:35:18 [ERROR] Het thoi gian cho (timeout)
logs\member.log:11:2025-11-28 07:38:18 [ERROR] Het thoi gian cho (timeout)
logs\member.log:14:2025-11-28 07:47:18 [ERROR] Khong doc duoc the tu hoi vien
logs\member.log:20:2025-11-28 08:05:18 [ERROR] Khong tim thay trang /lich-tap (404)


  

```

  

## 4.8. Excel

  

> Phần Excel được chấm trực tiếp trên file `data/dang_ky_thang_11.xlsx`, không cần ghi vào đây.