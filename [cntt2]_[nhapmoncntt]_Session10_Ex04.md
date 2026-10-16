

# PHẦN 1. THIẾT KẾ KIẾN TRÚC PROMPT (BẢN PROMPT HOÀN CHỈNH)

Dưới đây là bản Prompt hoàn chỉnh viết bằng Markdown theo đúng cấu trúc 3 phần và các ràng buộc đã đề ra:
```
# VAI TRÒ VÀ BỐI CẢNH
Bạn là một gia sư AI thân thiện, tận tâm và có khả năng sư phạm xuất sắc. Nhiệm vụ của bạn là giải thích khái niệm "Mô hình IPO (Input - Process - Output) trong trang trại thông minh" cho một sinh viên năm 1 mới bắt đầu học, chưa có nhiều kiến thức nền tảng về nông nghiệp thông minh hay CNTT.

## YÊU CẦU CỤ THỂ 
Hãy thực hiện các công việc sau đây theo dạng danh sách nhiệm vụ:
- [ ] Giải thích khái niệm mô hình IPO (Input - Process - Output) một cách đơn giản, dễ hiểu nhất
- [ ] Đưa ra 1 ví dụ thực tế, gần gũi trong trang trại thông minh (ví dụ: tưới nước tự động, quản lý nhiệt độ nhà kính...)
- [ ] Phân tích rõ từng thành phần trong ví dụ: Cái gì là Input? AI/Hệ thống làm gì ở phần Process? Kết quả thu được ở Output là gì?
- [ ] Tóm tắt bài học trong 2 - 3 câu ngắn gọn để sinh viên dễ nhớ lâu
- [ ] Trình bày bằng văn phong mộc mạc, ngắn gọn, có gạch đầu dòng rõ ràng
```
# PHẦN 2. GIẢI PHÁP CHO TRƯỜNG HỢP KIỂM THỬ

- Nếu AI trả về kết quả quá dài hoặc chứa toàn thuật ngữ tiếng Anh chuyên môn làm sinh viên năm 1 bị "ngợp"

**Các ràng buộc đã cài cắm trong Prompt để kiểm soát:**

1.  Ràng buộc độ dài  Giới hạn cứng tổng độ dài không vượt quá 400 từ giúp ngăn chặn việc AI sinh ra văn bản quá dài.
    
2.  Ràng buộc ngôn ngữ và thuật ngữ 
    
    -   Yêu cầu bắt buộc dịch/chú thích nghĩa tiếng Việt ngay bên cạnh từ tiếng Anh (`Input (Đầu vào)`, `Process (Xử lý)`, `Output (Đầu ra)`).
3.  Ràng buộc đối tượng mục tiêu: Xác định rõ đối tượng nghe là sinh viên năm 1 chưa có nền tảng giúp AI điều chỉnh mô hình ngôn ngữ về mức độ bình dân, dễ hiểu nhất
# PHẦN 3. SẢN PHẨM (.MD): KẾT QUẢ PHẢN HỒI CỦA AI SAU KHI ÁP DỤNG PROMPT

Dưới đây là nội dung mẫu của file .md lưu lại câu trả lời chuẩn mực của AI:

Markdown

```
# GIẢI THÍCH MÔ HÌNH IPO TRONG TRANG TRẠI THÔNG MINH

Chào bạn! Đừng lo lắng nếu thấy khái niệm này lạ lẫm. **IPO** thực ra chỉ là viết tắt của 3 bước rất tự nhiên trong cuộc sống: **Đầu vào -> Xử lý -> Đầu ra**[cite: 2]. 

Hãy cùng tìm hiểu qua một ví dụ siêu đơn giản dưới đây nhé!

---

## 1. Mô hình IPO là gì?
IPO là cách một hệ thống thông minh làm việc, gồm 3 chặng[cite: 2]:
* **I - Input (Đầu vào):** Thu thập thông tin từ môi trường xung quanh.
* **P - Process (Xử lý):** Suy nghĩ, tính toán và đưa ra quyết định dựa trên thông tin nhận được.
* **O - Output (Đầu ra):** Thực hiện hành động cụ thể dựa trên quyết định đó.

---

## 2. Ví dụ thực tế: Hệ thống tưới nước tự động cho vườn dâu tây

Hãy tưởng tượng bạn có một trang trại dâu tây thông minh[cite: 2]. Mô hình IPO sẽ hoạt động như sau:

* 📥 **Input (Đầu vào):**
  * Các cảm biến cắm dưới đất đo được độ ẩm hiện tại của đất đang quá khô (chỉ còn 20%).
  * Dữ liệu độ ẩm này được gửi về máy tính trung tâm.

* ⚙️ **Process (Xử lý):**
  * Bộ xử lý (AI / Máy tính) nhận dữ liệu "20%".
  * Máy tính so sánh với mức chuẩn (đất trồng dâu cần độ ẩm 60%).
  * Máy tính đưa ra quyết định: *"Đất đang quá khô, cần phải bật máy bơm tưới nước ngay!"*

* 📤 **Output (Đầu ra):**
  * Hệ thống phát lệnh bật vòi phun nước tự động tưới cho luống dâu.
  * Khi độ ẩm đạt đủ 60%, máy tính nhận Input mới và ra lệnh tắt máy bơm.

---

## 💡 Tóm tắt ghi nhớ
> **Mô hình IPO trong trang trại thông minh** đơn giản là: Cảm biến thu thập dữ liệu (**Inpu
```
