# 1. Phân tích kiến trúc
## Đề xuất kiến trúc, giải thích lý do lựa chọn và ý nghĩa từng thành phần trong kiến trúc, vẽ biểu đồ package mô tả kiến trúc.
### Đề xuất kiến trúc
#### Presentation Layer (Giao diện người dùng)
Cho phép người dùng nhập bảng chấm công và chọn phương thức thanh toán.
#### Service Layer (Tầng dịch vụ)
Xử lý logic nghiệp vụ như tính toán lương, kiểm tra bảng chấm công, và quản lý phương thức thanh toán.
#### Data Access Layer (Tầng truy xuất dữ liệu): 
Giao tiếp với cơ sở dữ liệu, đọc/ghi thông tin nhân viên, lương.
#### Storage Layer (Tầng lưu trữ): 
Bao gồm cơ sở dữ liệu tiền lương và cơ sở dữ liệu quản lý dự án hiện có.

![](https://www.planttext.com/api/plantuml/png/Z9EnIiH048RxVOhX-ciiBUGq0GiNGGo7xP8BIRZShYGxHH1h2vyYnI7OU8BLfR08t7la2Nm5PvNRIsuZfahOsU-VcVzdl-hFMQ55hd6LiMAPIiXL4J5sByAbY2EONAP2-MaahsDKgOyodi030mWpKHHWYucGS_ewXHiKCiXJzjXHzDlwEKnWtjRhhjRliJaD2EIeP3nGynAnyePB0GsH14h8NhUWtRx8688SIxZ3ThlM1da3dhRr4tO7k4eKHwIBpZQsudJtRdrkTkIbZ-VIlpWPwirt6wG1g6ktdK4Fcn9sR2PCfsT3hi0fwDrcLz6VRggG7Naz5XkwqaVtsn9PDgy88Qs38pWRn5-W5JQSOovH6ULKmiBabFtan8RKUxHrxH-wDxCJdwLrqdmOf-X1aD0xD9LaxgHxZQx9cKcxszmTSHJ6Pf5Sc5Vv3G00__y30000)