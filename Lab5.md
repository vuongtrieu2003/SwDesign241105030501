# Lab 5
Thiết kế các hệ thống con trong hệ thống Payroll System
## 1. Security Subsystem:
- Hệ thống này đảm bảo an toàn cho hệ thống Payroll:
   + Xác thực người dùng (login).
   + Phân quyền truy cập theo vai trò.
   + Quản lý các phiên làm việc và kiểm soát truy cập cho từng chức năng.
- Thành phần chính:
  + `LoginForm:` Giao diện để người dùng nhập thông tin đăng nhập.
  + `AuthenticationService:` Xác thực thông tin đăng nhập từ cơ sở dữ liệu người dùng.
  + `AccessControl:` Quản lý quyền truy cập dựa trên vai trò.
  + `SessionManager:` Quản lý các phiên làm việc của người dùng.
  + `UserDatabase:` Lưu trữ thông tin người dùng.
    
![](https://www.planttext.com/api/plantuml/png/X9C_JiCm5CRtdCBgL2HwWGXLXI8GWag8mW5Snqgi9i_1Te8gn80Oc3a0WWuiI9KOM6W6XbJSmoVW2jX9q_z0bYJFdt_Vb_VYx-op9HKMAeb2H_OP8C4bTKY8fKGdt6Tmm4M4hXrahqHI0JYYBkegmS0lgx7HNd7XBLTbqekOgc-vAENCSswSANGtKG45nGXMZ4ENYfGHMXcaE6GULhGjg6T5E9JrLTFjDKFZiSTvI36K5BFCV3WpbMBpqQ9m6d4UXn0gPPk34ZoiOf20aluf5H4p90vrixHWZubDli5y1ktIOby70_QfgAX5dwTBwy6ABXKw2bwbakLzNJYpkZ2SVQnm3ykgYmtBbYxgu7YdocnbpHBlKsNVrlfgqBPkqVF1DnhDNoRcejgXpaOCgI1_1nyfy-zC7YPtvX42FHx5DMVpHejSIcr8vo8Pe5IFNs0H1_xNcyuU6VBo3_3_uYrFqKRBXu0kau7ERWtIqib_cLQ6PY37WSwUp0VgyP2ZE63vAw0mVuvGodHsJsfEoupA7fmV0000__y30000)

## 2. Payroll Subsystem:
- Hệ thống này chịu trách nhiệm quản lý và xử lý toàn bộ nghiệp vụ tính lương:
  + Lấy dữ liệu chấm công và hợp đồng nhân viên để tính toán lương.
  + Xử lý thanh toán qua ngân hàng hoặc in phiếu lương.
  + Lưu trữ lịch sử thanh toán.
- Thành phần chính:
  + PayrollController: Điều phối các hoạt động tính lương.
  + PayrollDBManager: Lưu trữ thông tin thanh toán trong cơ sở dữ liệu.
  + SalaryCalculator: Tính toán lương dựa trên các điều kiện hợp đồng và chấm công.
  + Paycheck: Lưu thông tin phiếu lương cho từng nhân viên.

![](https://www.planttext.com/api/plantuml/png/T5BBQi905DtdAowk8YZTXo9ItGWLYWfTJvDB4fpC3VEGXj9rlyD5bwMkTU52y3_o1Vs59eunZQcpo8HpppdtpfdvsUs7IZEfJS8TjOm5I5Be-9mf1KyiayJvY8GkTvJmva2vKaa-AdMkkrqFLXG7jXQYGCaq5aK_Gd_fOf9ooX0dWGTpBMCH5logwhmxpMRZXoaJBBpqwgSMdw5FCb0UJ5bwRsrwbSRM1hQ_OYjiuAuyRLwJVJMpRafkpLnJwi7dZ3EPZHZt3MUQBY7vPmGjmOt8IFLCSec5QK3cXMCFIf1diu9LOTtgvyfbH4aIAnMJS1NZg6eF-Q_wRx2dgAkvscUpE4l82DtiNeG_FhcNtzAo_IJw_K7xxZpeF1utvcuXJGQl9jz-QWZotJVmEDzzcCuDdrQKXS_Yy2KYq7HO2-37pN4jmblooqbBMRvT4wHHd6_tfXOEKGJbK_y5003__mC0)

## 3. Timecard Subsystem:

