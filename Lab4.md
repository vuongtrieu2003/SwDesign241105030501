# Lab 4
## 1. Login:
### 1.1. Mô tả tương tác giữa các đối tượng thiết kế:
- Đối tượng:
  + `LoginForm`: Giao diện nhập thông tin người dùng.
  + `AuthenticationService`: Xác thực thông tin đăng nhập.
  + `Employee`: Đối tượng đại diện cho người dùng sau khi đăng nhập.
- Tương tác:
  + Người dùng nhập thông tin vào `LoginForm`.
  + `LoginForm` gửi yêu cầu đến `AuthenticationService` để xác thực.
  + Nếu thông tin hợp lệ, `AuthenticationService` tạo phiên làm việc với đối tượng `Employee`.
### 1.2. Đơn giản hóa sơ đồ tuần tự bằng hệ thống con:
- Hệ thống con liên quan:
  + `Authentication Subsystem`: Bao gồm `LoginForm` và `AuthenticationService`.
- Quy trình: Thay vì xử lý trực tiếp tất cả các logic trong giao diện, logic xác thực được chuyển cho `AuthenticationService`.
  
![](https://www.planttext.com/api/plantuml/png/T9B1IWCn48RlUOevjeU-m1waWgW7yM9zW6msx8Pk9pMR57kK7ZnuyW44br84eQ0WYCcXXos-Hvx0Lp3RLhk5zZQJcN_-RuRyk4Mtq5HfCyX9qHS8IXQSKAQbWkk2An9BWmbLOxYGgS1JgGQ4ITHAvd1iTCPH2qQra7Z5rKWmJXAgQKmBlfAVR192wWmwHzin4Lnctiw7eBFg0rFGmNpvk9o445S5yjzQw_QQHN3ctLp0k7ermBnzCN1RbIoCzEwTaRsQUbWJBOAUCcCOUJl39Wkcts_UFGb8gYzCILC2dSD0FUNjD4npTz3tTg7XnjGFhK0q7KBktJraqjjF1lsrrxRGFWIyUxQ6WmvXMVDcLIbsLc_SRhDl1EV2kmckEXx-DeshKa8h9C-O0Li3hV52cvrfY8E3Q9CknwJ-8xy0003__mC0)

### 1.3. Mô tả hành vi liên quan đến lưu trữ:
- Dữ liệu:
  + Tên người dùng và mật khẩu được truy xuất từ cơ sở dữ liệu `UserDatabase`.
  + Phiên làm việc được lưu tạm thời trong bộ nhớ ứng dụng.
### 1.4. Tinh chỉnh mô tả luồng sự kiện:
1. Người dùng mở `LoginForm`.
2. Nhập tên người dùng và mật khẩu.
3. `LoginForm` gửi thông tin đến `AuthenticationService`.
4. `AuthenticationService` truy vấn `UserDatabase` để kiểm tra thông tin.
5. Nếu hợp lệ:
    - Tạo đối tượng `Employee`.
    - Hiển thị thông báo đăng nhập thành công.
6. Nếu không hợp lệ, hiển thị thông báo lỗi.
### 1.5. Hợp nhất các lớp và hệ thống con:
- Các lớp liên quan:
  + `LoginForm`: Quản lý giao diện nhập liệu.
  + `AuthenticationService`: Xử lý xác thực.
  + `Employee`: Đại diện người dùng đã đăng nhập.
## 2. Maintain Timecard:
### 2.1. Mô tả tương tác giữa các đối tượng thiết kế:
- Đối tượng:
  + `TimecardForm`: Giao diện nhập thẻ chấm công.
  + `TimecardController`: Xử lý logic nghiệp vụ liên quan đến thẻ chấm công.
  + `Timecard`: Đối tượng lưu thông tin về giờ làm việc.
- Tương tác:
  + Nhân viên nhập thông tin thẻ chấm công vào `TimecardForm`.
  + Dữ liệu được chuyển đến `TimecardController` để xử lý và lưu vào cơ sở dữ liệu qua `DatabaseService`.
### 2.2. Đơn giản hóa sơ đồ tuần tự bằng hệ thống con:
- Hệ thống con liên quan:
  + `Timecard Management Subsystem`: Bao gồm `TimecardForm`, `TimecardController` và `DatabaseService`.
- Quy trình: Tách riêng giao diện nhập liệu (`TimecardForm`) và xử lý logic nghiệp vụ (`TimecardController`).

![](https://www.planttext.com/api/plantuml/png/V98_JiCm58Ttd-Adxhr01bI9lmFg0WEhurZ4mh4hsudKcO61Gz0WiI1LC33XWS5Ixv4JS0KS4jfGH1RBVjBxtlT-ygV_c5b7ZIiBIUoDK33QSaAPqmR7nKBg9UUW5fDv7XuLAX6UrOIakbGPDKjSYe8pQh8JRGh2j796ostni7jBRaX67KsfvJZgBnVSL89nGhP3fWU_Q0dcUVE-Ni3buKrTmqKt5oiUB9vF1LXR9iEM8M8tEy5fuzS2MUDV84NZxyenqAwnnUtf9ZZVl9P3fIgiDDYcXctymt06sMl5z1-xgr0pg7PN1TdJLoeVqVgJLBTWRvM6Me-0kg0YuYVu16TH-FOxNNy_f90PLrdxCRu0003__mC0)

### 2.3. Mô tả hành vi liên quan đến lưu trữ:
Dữ liệu: Thông tin thẻ chấm công (ngày làm việc, số giờ) được lưu vào bảng `Timecards` trong cơ sở dữ liệu.
### 2.4. Tinh chỉnh mô tả luồng sự kiện:
1. Nhân viên mở `TimecardForm`.
2. Nhập thông tin thẻ chấm công:
    - Ngày làm việc.
    - Số giờ làm.
3. Nhấn "Lưu" để gửi yêu cầu đến `TimecardController`.
4. `TimecardController` xác thực dữ liệu và lưu vào `DatabaseService`.
5. Hiển thị thông báo lưu thành công.
