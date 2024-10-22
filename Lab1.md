# LAB 1
PHÂN TÍCH KIẾN TRÚC, CƠ CHẾ, CA SỬ DỤNG

## 1. Phân tích kiến trúc
### Đề xuất kiến trúc, giải thích lý do lựa chọn và ý nghĩa từng thành phần trong kiến trúc, vẽ biểu đồ package mô tả kiến trúc.
#### Đề xuất kiến trúc
Kiến trúc phù hợp cho hệ thống này là kiến trúc phân lớp (Layered Architecture), với 4 lớp chính:

- Presentation Layer (Giao diện người dùng): Cho phép người dùng nhập bảng chấm công và chọn phương thức thanh toán.
- Service Layer (Tầng dịch vụ): Xử lý logic nghiệp vụ như tính toán lương, kiểm tra bảng chấm công, và quản lý phương thức thanh toán.
- Data Access Layer (Tầng truy xuất dữ liệu): Giao tiếp với cơ sở dữ liệu, đọc/ghi thông tin nhân viên, lương.
- Storage Layer (Tầng lưu trữ): Bao gồm cơ sở dữ liệu tiền lương và cơ sở dữ liệu quản lý dự án hiện có.

**Biểu đồ package:**
  
![](https://www.planttext.com/api/plantuml/png/Z9EnIiH048RxVOhX-ciiBUGq0GiNGGo7xP8BIRZShYGxHH1h2vyYnI7OU8BLfR08t7la2Nm5PvNRIsuZfahOsU-VcVzdl-hFMQ55hd6LiMAPIiXL4J5sByAbY2EONAP2-MaahsDKgOyodi030mWpKHHWYucGS_ewXHiKCiXJzjXHzDlwEKnWtjRhhjRliJaD2EIeP3nGynAnyePB0GsH14h8NhUWtRx8688SIxZ3ThlM1da3dhRr4tO7k4eKHwIBpZQsudJtRdrkTkIbZ-VIlpWPwirt6wG1g6ktdK4Fcn9sR2PCfsT3hi0fwDrcLz6VRggG7Naz5XkwqaVtsn9PDgy88Qs38pWRn5-W5JQSOovH6ULKmiBabFtan8RKUxHrxH-wDxCJdwLrqdmOf-X1aD0xD9LaxgHxZQx9cKcxszmTSHJ6Pf5Sc5Vv3G00__y30000)
## 2. Cơ chế phân tích:
**Các cơ chế cần giải quyết trong bài toán bao gồm:**
- Cơ chế xử lý bảng chấm công: Hệ thống cần ghi lại thời gian làm việc của nhân viên và tính số giờ làm thêm theo đúng quy định.
- Cơ chế tính toán lương: Hệ thống phải có khả năng tính chính xác lương của nhân viên theo giờ, nhân viên hưởng lương cố định và nhân viên hưởng hoa hồng.
- Cơ chế chọn phương thức thanh toán: Mỗi nhân viên có thể chọn phương thức thanh toán khác nhau (chuyển khoản hoặc nhận trực tiếp).
- Cơ chế báo cáo: Cần cung cấp báo cáo về số giờ làm việc, tổng lương và chi tiết liên quan cho từng nhân viên.
- Tích hợp với cơ sở dữ liệu cũ: Hệ thống phải tích hợp với cơ sở dữ liệu cũ và kiểm tra sự hợp lệ.
## 3. Phân tích ca sử dụng Payment:
**Lớp phân tích: Bao gồm các lớp chính:**
- Employee: Nhân viên chọn phương thức thanh toán.
- PayrollService: Xử lý yêu cầu tính lương và thanh toán.
- PaymentMethod: Phương thức thanh toán được chọn (chuyển khoản, nhận phiếu lương).
- Paycheck: Tạo phiếu lương.

**Biểu đồ sequence:**

![](https://www.planttext.com/api/plantuml/png/R95BYW8n48RtEKLTe2_G328CBWT6TE4sn622wKgJhXOyX7UOB5m82iwsU-4Yu3roWhd2nFTpLHH_rV_Luw_TTIlYZkh2i6gg4Poj9EE2h8DUKHexbvALgK0BNN8a-EPpPuqPI3VJuaKg9DAN96N7pufGKamPktX2rdcook5JnNQ1KAhzTkzn0fJobKY1emAomIDxR3cRtA0v3CCc5PkJ0tiGto7xTV10BgmFX1i7b0q_21IR9Rrd7jT9kDXucoRMiTdLzzZxZeyikzuoXr7m0b35PeDWOllBGHptPbs9uyCR_W400F__0m00)

**Biểu đồ lớp mô tả các lớp phân tích:**

![](https://www.planttext.com/api/plantuml/png/Z58xQWCn4ErrYYcJmXTG4HnmYXI1W7C1HJjaXVMBFeObv32k0e50watXmk1xx0boXMW_idSN5r4XDE_Dp9idwVTdl_I1kH2L97uZD3ZZaN39l8SxPQMf4E6DG5euXFSh2klWX7xfOCqKJW3BAeKwF60eJK7XSHns2GvV8_em45VN5BP65EIT3Bg9S4RADRgju5dTzk2AXQJMxXczLIRgGA4myLdsA6UIHvboKgUs_PXosEEyHBvfoNoUw9yd7kHL5pnLTkRL6OxUPojiCiibOvtKsTA_x3ZanXNZcNFRqmij5ZVpQwDG7JuZyAR-Y6J63UaZbnJ2uKkN88_VnrqoTxcWdpxbDlNEW2r5K-_ZgMQ9kcZ_qHy0003__mC0)
