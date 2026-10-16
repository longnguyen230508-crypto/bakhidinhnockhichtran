

# HƯỚNG DẪN CÀI ĐẶT CẢM BIẾN ĐỘ ẨM CHO LAN

## 1. CHUẨN BỊ THIẾT BỊ
- Cảm biến độ ẩm `DHT22`
- Raspberry Pi / SoC
- Dây nối Dupont, tua vít

---

## 2. BẢNG SO SÁNH CẢM BIẾN
| Tiêu chí | DHT11 (Cũ) | DHT22 (Mới) |
| :--- | :--- | :--- |
| **Độ ẩm** | Thấp | Cao|
| **Nhiệt độ** | 0 C - 50 c| 40 C - 80 c |

---

## 3. CÁC BƯỚC CÀI ĐẶT
### Bước 1: Cập nhật hệ thống
> mở terminal và cập nhật danh sách gói
> 
`sudo apt update && sudo apt upgrade -y `


### Bước 2: Cài đặt thư viện
> cài đặt thư viện đọc dữ liệu từ cảm biến
> 
`
sudo apt install -y git python3-pip
sudo pip3 install Adafruit_DHT
`

### Bước 3: Kích hoạt 1-Wire
> bật giao tiếp 1-Wire trên hệ thống
> 
`
sudo raspi-config    \# Chọn: Interface Options > 
1-Wire > Enable
`

### Bước 4: Kiểm tra kết nối
> sau khi bật 1-Wire, kiểm tra thiết bị
> 
`
ls /sys/bus/w1/devices/    \# Kết quả dạng 28-\*xxxxxxx
`

### Bước 5: Đọc dữ liệu cảm biến
> tải và chạy file python mẫu
> 
`
git clone https://github.com/adafruit/Adafruit_Python_DHT.git
cd Adafruit_Python_DHT/examples
python3 AdafruitDHT.py 22 4    \# 22: DHT22, 4: GPIO pin
`
### Bước 6: tự động chạy sau khi khởi động (tùy chọn)
> thêm vào crontab để đọc dữ liệu định kỳ
>
`
crontab -e    \# thêm dòng ( vd mỗi 5p):
*/5 * * * * python3 /home/pi/read_dht22.py
`

---

## 4. SƠ ĐƠ KẾT NỐI & KIỂM TRA
- **VCC** $\rightarrow$ `3.3V (Pin 1)`
- **GND** $\rightarrow$ `GND (Pin 6)`
- **DATA** $\rightarrow$ `GPIO4 (Pin 7)`

### Task List kiểm tra:
- [x] Đã cắm đúng chân phần cứng
- [x] Cài đặt thành công thư viện
- [ ] Kiểm tra giá trị độ ẩm lý tưởng ($60\% - 80\%$)
