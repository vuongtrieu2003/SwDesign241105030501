# Lab 4
## 1. Login
### 1.1. Mô tả tương tác giữa các đối tượng thiết kế:
- Đối tượng:
  + LoginForm: Giao diện nhập thông tin người dùng.
  + AuthenticationService: Xác thực thông tin đăng nhập.
  + Employee: Đối tượng đại diện cho người dùng sau khi đăng nhập.
- Tương tác:
  + Người dùng nhập thông tin vào LoginForm.
  + LoginForm gửi yêu cầu đến AuthenticationService để xác thực.
  + Nếu thông tin hợp lệ, AuthenticationService tạo phiên làm việc với đối tượng Employee.
