

### PHẦN 1. PHÂN TÍCH SAI LẦM VÀ ĐẶC TÍNH KỸ THUẬT

#### 1. Hai sai lầm trong tư duy của Nam khi dùng file Rich Text (.docx) cho lưu trữ mã nguồn:

-   Sai lầm về khả năng cộng tác và kiểm soát phiên bản: Nam dùng file `.docx` (định dạng nhị phân - binary) lưu trữ trên Git. Git được thiết kế để quản lý mã nguồn dạng văn bản thuần túy (plain text). Khi lưu file `.docx`, Git không đọc được nội dung bên trong mà chỉ xem đó là một cục dữ liệu lớn, dẫn đến việc xung đột toàn bộ file khi có hai người cùng sửa.
    
-   Sai lầm về trải nghiệm xem trực tiếp: Nam chọn định dạng Word với suy nghĩ "cho dễ trình bày", nhưng lại bỏ qua việc GitHub không hỗ trợ render trực tiếp file `.docx` trên trình duyệt, khiến các thành viên trong nhóm buộc phải tải file về máy mỗi khi muốn đọc.
    

#### 2. So sánh khả năng chống lỗi mạng giữa `.docx` và Markdown:

-   **Đặc tính của file `.docx` (Bẫy dữ liệu):** Thực chất file `.docx` là một gói nén ZIP chứa nhiều tệp XML bên trong. Nếu quá trình tải lên/tải xuống gặp lỗi mạng làm mất hoặc sai lệch dù chỉ 1 byte dữ liệu, cấu trúc của gói nén bị phá vỡ hoàn toàn, khiến file `.docx` trở nên hỏng và không thể mở được.
    
-   Đặc tính của file Markdown (`.md`): Markdown là văn bản thuần túy (plain text). Nếu bị mất hoặc lỗi một vài ký tự do truyền tải mạng, người dùng vẫn có thể mở file bằng bất kỳ trình soạn thảo văn bản nào để đọc phần nội dung còn lại hoặc sửa thủ công một cách dễ dàng mà không làm hỏng toàn bộ tài liệu. Ngoài ra, dung lượng của Markdown vô cùng nhẹ và Git có thể theo dõi từng dòng thay đổi nhỏ nhất.
    

### PHẦN 2. HOÀN THIỆN: CHUYỂN ĐỔI SANG MARKDOWN (.MD)

Dưới đây là nội dung giới thiệu dự án "GreenTech" sau khi được chuyển đổi từ định dạng Word sang chuẩn **Markdown (`.md`)** để sử dụng trên StackEdit và GitHub:
```
#  GREEN TECH

> **Technology for a Greener Future**

## 1. Giới thiệu
GreenTech là dự án hướng tới việc ứng dụng công nghệ để bảo vệ môi trường, giúp cuộc sống xanh và bền vững.

## 2. Mục tiêu
- Tạo ra giải pháp công nghệ xanh.
- Nâng cao ý thức cộng đồng.
- Phát triển bền vững.

---

```
