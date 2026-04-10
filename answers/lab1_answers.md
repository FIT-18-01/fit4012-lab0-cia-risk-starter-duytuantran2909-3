# Lab 01 Answers
## CIA & Risk: Hệ thống lưu điểm

**Họ và tên:** Trần Duy Tuấn

**MSSV:** 1876102004

**Lớp/Nhóm:** CNTT 18-01

---

## 1. Assets
Liệt kê ít nhất 2 assets cần bảo vệ.

- Asset 1:Cơ sở dữ liệu điểm số (Grade Database): Chứa dữ liệu quan trọng nhất của hệ thống.


- Asset 2: Thông tin định danh người dùng (User Credentials): Tài khoản và mật khẩu của giảng viên và sinh viên.

---

## 2. Mapping CIA
Ghép từng sự cố với CIA.

- Sự cố A -> Một số sinh viên không đăng nhập được -> Availability (A)
- Sự cố B -> Điểm của một sinh viên bị đổi từ 8.0 thành 5.0 ->Integrity (I)
- Sự cố C -> Danh sách điểm bị lộ ra ngoài nhóm chat ->Confidentiality (C)

---

## 3. Phân tích sự cố B
- Threat: Kẻ tấn công chiếm quyền điều khiển tài khoản giảng viên hoặc người nội bộ cố tình thay đổi dữ liệu trái phép.
- Vulnerability: Hệ thống thiếu cơ chế xác thực đa yếu tố (MFA) hoặc không có hệ thống ghi nhật ký (Audit Logs) để theo dõi các thao tác chỉnh sửa điểm.
- Mitigation: Triển khai xác thực 2 lớp (MFA) cho tài khoản giảng viên và xây dựng hệ thống Logging ghi lại chi tiết: ai sửa, sửa lúc nào, giá trị cũ và mới. 

---

## 4. Reflection
Viết 5-7 dòng.
Nếu là quản trị viên, em sẽ ưu tiên xử lý Sự cố B (Integrity) trước. Bởi vì tính toàn vẹn của dữ liệu điểm là giá trị cốt lõi của hệ thống này. Nếu điểm số bị thay đổi mà không thể kiểm soát, hệ thống sẽ mất hoàn toàn uy tín và gây hậu quả nghiêm trọng cho sinh viên. Tiếp theo sẽ là sự cố C để bảo vệ quyền riêng tư, và cuối cùng là sự cố A để khôi phục dịch vụ.


---

## 5. Bonus Flag
`FIT4012{A-?-B-?-C-?}`

Flag của em:
FIT4012{A-A-B-I-C-C}

