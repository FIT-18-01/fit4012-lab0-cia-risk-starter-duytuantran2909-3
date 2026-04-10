# FIT4012 - Report 1 Page
## Lab 01 - CIA & Risk: Hệ thống lưu điểm

### 1. Mục tiêu bài lab
- Nhận diện tài sản cần bảo vệ trong một hệ thống thông tin đơn giản.
- Phân biệt Confidentiality, Integrity, Availability.
- Xác định threat, vulnerability, mitigation.
- Thực hành workflow GitHub cơ bản để nhận và nộp bài.

### 2. Cách làm
- Đọc bối cảnh và xác định các thành phần quan trọng của hệ thống.
- Phân tích từng sự cố theo bộ ba CIA.
- Chọn sự cố B để phân tích sâu hơn theo threat - vulnerability - mitigation.
- Hoàn thiện bài làm trong repo và commit/push lên GitHub.

### 3. Kết quả chính
**Assets:**
- Cơ sở dữ liệu điểm số: Lưu trữ kết quả học tập của toàn bộ sinh viên, là tài sản quan trọng nhất.
- Hệ thống xác thực người dùng: Bao gồm thông tin tài khoản (ID, mật khẩu) của giảng viên và sinh viên để kiểm soát quyền truy cập.

**CIA mapping:**
- Sự cố A -> Availability: Hệ thống bị gián đoạn, sinh viên không thể truy cập dịch vụ khi cần.
- Sự cố B -> Integrity: Dữ liệu điểm bị thay đổi sai lệch so với thực tế, làm mất tính toàn vẹn.
- Sự cố C -> Confidentiality: Thông tin riêng tư bị rò rỉ ra bên ngoài cho những người không có thẩm quyền.

**Phân tích sự cố B:**
- Threat: Kẻ tấn công (Hacker) chiếm quyền tài khoản hoặc người nội bộ (Insider) cố tình chỉnh sửa dữ liệu trái phép.
- Vulnerability: Hệ thống thiếu cơ chế xác thực đa yếu tố (MFA) và không có hệ thống ghi nhật ký (Audit Log) để truy vết thao tác.
- Mitigation: Triển khai xác thực 2 lớp (MFA) cho tài khoản có quyền ghi và thiết lập Logging ghi lại chi tiết lịch sử thay đổi dữ liệu (ai sửa, sửa lúc nào).

### 4. Kết luận ngắn
Qua bài lab này, em đã nắm vững quy trình làm việc với Git/GitHub và hiểu rằng An toàn thông tin là sự phối hợp chặt chẽ giữa cả ba yếu tố CIA. Phần khó nhất là việc xác định chính xác các Vulnerability tiềm ẩn từ một sự cố thực tế. Bài học quan trọng nhất là khi thiết kế hệ thống, cần chú trọng đến tính toàn vẹn (Integrity) và phải có cơ chế ghi log đầy đủ để có thể ứng phó và xử lý khi sự cố xảy ra.