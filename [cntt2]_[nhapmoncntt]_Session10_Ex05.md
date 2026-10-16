
# Smart-Farm: Hệ Thống IoT Cho Trang Trại Lan

> Hệ thống quản lý, giám sát và tưới tự động cho trang trại Lan.

### 1. Phân Tích Hệ Thống

-   **Input:** Cảm biến đo nhiệt độ, độ ẩm, ánh sáng, EC, pH; Tín hiệu điều khiển từ App.
    
-   **Output:** Bật/tắt bơm tưới, quạt, đèn; Gửi cảnh báo về App.
    

### 2. Cài Đặt
> mã: 
```
git clone https://github.com/smart-farm/lan-farm-iot.git
cd lan-farm-iot && pip install -r requirements.txt
python3 main.py --mode=production

```

### 3. Tính Năng Cốt Lõi

-   [x] Giám sát môi trường thời gian thực.
    
-   [x] Tưới tự động & cảnh báo khi vượt ngưỡng.
    
-   [x] Điều khiển thủ công / tự động.
    
-   [x] Xuất báo cáo Excel/PDF.
    

### 4. Chu Kỳ Fetch–Decode–Execute Khi Nhận Lệnh Tưới

>  **CPU xử lý lệnh tưới Lan:**
> 
> 1.  Fetch: Lấy mã lệnh `0xA1` (Bật bơm) từ RAM vào thanh ghi.
>     
> 2.  Decode: Giải mã `0xA1` thành lệnh kích hoạt chân GPIO đóng Relay.
>     
> 3.  Execute: Xuất tín hiệu HIGH ra chân GPIO để bật máy bơm tưới Lan.
>     

### 5. Kim Tự Tháp DIKW: Từ Nhiệt Độ Đến Hành Động Tưới

```
Action --> Bật bơm tưới phun sương làm mát
Knowledge --> Lan bị héo khi nhiệt độ > 30 C quá 15 phút
Information --> Nhiệt độ hiện tại: 32 C (Vượt ngưỡng 30°C)
Data --> Cảm biến gửi chỉ số thô: "32"

```

### 6. Bảng Bảng Thông Số Môi Trường

**Thông số**

**Ngưỡng An toàn**

**Ngưỡng Nguy hiểm**

**Thiết bị can thiệp**

**Nhiệt độ**

22 C - 28 C

> 30 C

Quạt + Phun sương

**Độ ẩm đất**

60% - 75%

< 50%

Bơm tưới gốc

### 7. Lưu Ý An Toàn & Xử Lý Sự Cố RAM Đầy

-   Bảo trì: Vệ sinh cảm biến 2 tuần/lần; ngắt điện trước khi sửa chữa.
    
-   Sự cố RAM đầy do log: Chạy lệnh `echo "" > /var/log/smartfarm.log` rồi khởi động lại dịch vụ `sudo systemctl restart smartfarm.service` để xóa bộ đệm an toàn.
