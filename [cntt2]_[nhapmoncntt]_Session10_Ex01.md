


# Hướng dẫn cài đặt và thiết lập VS Code cho lớp học

Tài liệu này sẽ hướng dẫn các bước cài đặt phần mềm Visual Studio Code (VS Code), cấu hình môi trường và kiểm tra tiến độ làm việc cho các thành viên trong lớp.

---

## 1. Yêu cầu hệ thống và chuẩn bị
Trước khi bắt đầu, hãy đảm bảo máy tính của bạn đã được kết nối Internet ổn định. Chúng ta sẽ sử dụng biến môi trường `PATH` để quản lý các công cụ dòng lệnh.

## 2. Các bước cài đặt vs code

Quy trình cài đặt Visual Studio Code được thực hiện qua 5 bước cơ bản như sau:

-   Bước 1: Tải về (Download). Truy cập trang web chính thức [code.visualstudio.com](http://code.visualstudio.com/) để tải bản cài đặt mới nhất phù hợp với hệ điều hành của bạn (Windows, Linux, hoặc macOS).
    
-   Bước 2: Cài đặt (Install). Khởi chạy tệp tin vừa tải về và làm theo các bước hướng dẫn trên màn hình để hoàn tất quá trình cài đặt.
    
-   Bước 3: Mở Terminal (Open Terminal). Mở trình điều khiển terminal trong máy (hoặc nhấn tổ hợp phím Ctrl + ngay trong VS Code > chọn New Terminal).
    

Bước 4: Thêm vào PATH - Không bắt buộc (Add to PATH). Cài đặt lệnh code để có thể mở VS Code nhanh chóng từ bất kỳ thư mục nào bằng lệnh:  
bash  
code --install-extension ms-vscode.vscode

-   Hãy thận trọng khi sử dụng mã.
    

Bước 5: Xác minh (Verify). Kiểm tra lại xem quá trình cài đặt đã thành công chưa bằng cách chạy lệnh kiểm tra phiên bản:  
bash  
code --version

-   Hãy thận trọng khi sử dụng mã.
## 3. câu lệnh python 

def chao_mừng_lớp_học(ten_mon):
    print(f"Chào mừng các bạn đến với môn {ten_mon}!")
    
if name == "main":
    mon_hoc = "Nhập môn Công nghệ Thông tin"
    chao_mừng_lớp_học(mon_hoc))
