# 1. Phân tích ca sử dụng Create Administrative Report
**Các lớp phân tích:**
  + PayrollAdministrator: Người dùng hệ thống có quyền tạo và lưu báo cáo hành chính.
  + ReportCriteria: Lớp lưu trữ các tiêu chí cho báo cáo, bao gồm loại báo cáo, ngày bắt đầu/kết thúc và tên nhân viên.
  + ReportGenerator: Lớp chịu trách nhiệm tạo báo cáo dựa trên các tiêu chí được cung cấp.
  + Report: Lớp đại diện cho báo cáo cuối cùng được tạo, có thể được xem và lưu trữ.
  + FileManager: Quản lý việc lưu trữ báo cáo, bao gồm yêu cầu nhập tên và vị trí lưu báo cáo.

**Biểu đồ sequence**
![Sequence Diagram](https://www.planttext.com/api/plantuml/png/T9B1IWCn48RlUOgX9ptu0ZsKbe9wK2dYnMFS3TrWcfGaM-ZPauW7tq0H4GeBUdHpy13nFV84leAJhMopBLucCCpt__CF-N6VGsEfjkLC47FD9MXb612QMQMXDw5BhOI0KJxZaXkhARPxG0sCuW0XpGC70pXdSwNjM7FBDAVGXqk_AY4BzMi9DjHF2guybWmBsPfjwICcMUE0-BYKquY_pC7oHghmrOx6XcX5aBte-a4Ut3i5g_rA9c9_4f5Sf-Z3CG_k1cUAuEuI_kl1Fwz3RF8USi5EgQHJfhjXnVTRcR1xrdyiqI-uUxbFKYhnFIj2NM7GkE32Fy8Y-kE-LQFsdsbweXroswezpabtFuHKuXSNlSN0s9058KCcy_WpVW400F__0m00)

- Xác định một số thuộc tính và quan hệ giữa các lớp phân tích:
  + Lớp PayrollAdministrator:
    * Nhiệm vụ: Yêu cầu tạo báo cáo và có thể lưu báo cáo.
    * Thuộc tính: adminID, name.
    * Quan hệ: Kết nối với ReportCriteria để nhập tiêu chí và với FileManager để lưu báo cáo.
  + Lớp ReportCriteria:
    * Nhiệm vụ: Lưu trữ tiêu chí báo cáo như loại báo cáo, ngày bắt đầu/kết thúc và tên nhân viên.
    * Thuộc tính: reportType, startDate, endDate, employeeNames.
    * Quan hệ: Cung cấp thông tin cho ReportGenerator để tạo báo cáo.
  + Lớp ReportGenerator:
    * Nhiệm vụ: Tạo báo cáo dựa trên tiêu chí từ ReportCriteria.
    * Thuộc tính: reportID, generationDate
    * Quan hệ: Nhận tiêu chí từ ReportCriteria và tạo đối tượng Report.+ 
  + Lớp Report:
    * Nhiệm vụ: Đại diện cho báo cáo cuối cùng có thể xem hoặc lưu trữ.
    * Thuộc tính: content, format, createdDate.
    * Quan hệ: Được tạo bởi ReportGenerator và có thể được lưu bởi FileManager.
  + Lớp FileManager:
    * Nhiệm vụ: Quản lý việc lưu báo cáo theo tên và vị trí được cung cấp.
    * Thuộc tính: filePath, fileName.
    * Quan hệ: Nhận thông tin từ PayrollAdministrator để lưu Report.
      
**Biểu đồ lớp**

![Class Diagram](https://www.planttext.com/api/plantuml/png/X59BRi8m4DtFANo1NA6Y8W9r0KA82uoI0IpiSJIUBgAg9-k28_KA1CUGr6hLtPlFUpDlxE-lwo8gYhvx1_5YsKY818t36CqEUmdElRRUieqgg47C1nXJ6Rpdtkg46Jt19sJIdheWkXIh91PpkwJaeUyeXMbYZJf6nEs4VUT2JxGTD6CfkYQc-HAZQjxYD1Pju2HMK3EZ2Qp4cl0nYCSHDa83f_r9N5b76sGyqMFUSSZiKC_FO9kT_tgegdefZW75RQQEfpCedKuz_qtvkpvp0dDNCouiXbUu_u4R0000__y30000)
- Giải thích biểu đồ lớp trong hệ thống Create Administrative Report:
  + PayrollAdministrator cung cấp tiêu chí báo cáo qua ReportCriteria và yêu cầu ReportGenerator tạo báo cáo.
  + ReportGenerator tạo báo cáo dựa trên thông tin từ ReportCriteria và cung cấp Report cuối cùng.
  + PayrollAdministrator có thể lưu Report thông qua FileManager, nơi quản lý tên và vị trí lưu trữ.
# 2. Phân tích ca sử dụng Create Employee Report
**Các lớp phân tích:**
**Biểu đồ sequence**
**Biểu đồ lớp**
# 3. Phân tích ca sử dụng Login
**Các lớp phân tích:**
**Biểu đồ sequence**
**Biểu đồ lớp**
# 4. Phân tích ca sử dụng Maintain Employee Information
**Các lớp phân tích:**
**Biểu đồ sequence**
**Biểu đồ lớp**
# 5. Phân tích ca sử dụng Maintain Purchase Order
**Các lớp phân tích:**
**Biểu đồ sequence**
**Biểu đồ lớp**
# 6. Phân tích ca sử dụng Run Payroll
**Các lớp phân tích:**
**Biểu đồ sequence**
**Biểu đồ lớp**
