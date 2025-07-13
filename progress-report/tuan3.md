# 📅 Tuần 3: Hiện thực hóa chức năng chính

## ✅ Mục tiêu công việc
- Cài đặt kiến trúc ứng dụng Android bằng Kotlin
- Xây dựng chức năng xem bài học (lý thuyết)
- Thiết kế và xử lý logic phần làm bài trắc nghiệm
- Kiểm tra hoạt động chuyển màn hình, lưu trạng thái cơ bản

## 🔨 Nội dung đã thực hiện

### 1. Cấu trúc dự án Android
- Tạo project Android mới: `InformaticsReviewApp`
- Thiết lập cấu trúc thư mục chuẩn MVVM:
📁 ui → Giao diện, màn hình
📁 model → Dữ liệu câu hỏi, bài học
📁 data → Repository, Room Database
📁 utils → Các hàm tiện ích chung


### 2. Chức năng xem bài học (Lý thuyết)
- Tạo màn hình `TheoryActivity`
- Dữ liệu lý thuyết (HTML/text) được load từ file JSON hoặc Room
- Bổ sung ảnh minh họa sinh động
- Có nút "Bắt đầu ôn tập" → chuyển sang phần câu hỏi

### 3. Chức năng trắc nghiệm
- Tạo `QuizActivity`:
- Hiển thị từng câu hỏi + 4 đáp án
- Người dùng chọn đáp án → lưu kết quả
- Dữ liệu câu hỏi dạng model:
```kotlin
data class Question(
    val id: Int,
    val content: String,
    val options: List<String>,
    val answer: Int
)
- Xử lý chấm điểm sau khi hoàn thành tất cả câu hỏi
4. Chuyển màn hình & xử lý trạng thái
•	Chuyển màn hình bằng Intent
•	Truyền dữ liệu bằng Bundle
•	Giữ trạng thái làm bài khi xoay màn hình (dùng ViewModel)
💡 Công nghệ & thư viện sử dụng
•	Kotlin (ngôn ngữ chính)
•	Room (lưu trữ offline dữ liệu bài học & câu hỏi)
•	Material Components (tạo UI đẹp, dễ thao tác)
•	ViewModel + LiveData (quản lý trạng thái UI)
📌 Kết quả đạt được
•	Đã xây dựng thành công 2 chức năng cốt lõi: xem bài học và làm bài trắc nghiệm
•	Tổ chức code rõ ràng theo kiến trúc MVVM
•	Giao diện có thể thao tác thử trên điện thoại/emulator
📝 Ghi chú
•	Chưa có tính năng thống kê điểm
•	Sẽ bổ sung chức năng lưu kết quả & bảng xếp hạng trong tuần sau
