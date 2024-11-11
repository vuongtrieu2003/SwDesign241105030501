# 1. Phân tích ca sử dụng Create Administrative Report
**Các lớp phân tích:**
- PayrollAdministrator: Người dùng (quản trị viên) khởi tạo yêu cầu báo cáo.
- ReportGenerator: Xử lý yêu cầu tạo báo cáo theo các tiêu chí được cung cấp.
- ReportCriteriaValidator: Kiểm tra tiêu chí báo cáo đã đầy đủ và hợp lệ chưa.
- ReportRepository: Lưu trữ hoặc loại bỏ báo cáo dựa trên yêu cầu.
- ErrorHandler: Hiển thị thông báo lỗi khi có sự cố hoặc thiếu dữ liệu.
  
**Biểu đồ sequence**

![Sequence Diagram](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3bTnTcQUGb5-SIfNOd99Vf52G69bKNvEZcDARcPUPd59KI9Ga0kRe8AkdK9GQa5-KObxQbugMCXA8VBmgbA5v8UxbfSgb3pSjJ1V8Uama4W64bneQX7QdOioIrABCXF34dCoKo36H1nUcAnGal5mzqOWbGasC-FmMWp3C7HYTLC8mW2WYOiB578Uxcx7xHnadOIzW2rah1GyCX_kRiu3-w0RIJyvmPXpR4CfEKv0Zed3g_8KoWulK2W3EQUa21WG85E9TuvpQLuwoAob1LZCmXsI8B8u4oXKQQNWWyqR20KAkjZiTOAfLpWoyV1YYACTKlDIGEaM0000__y30000)

**Thuộc tính và Quan hệ:**

- PayrollAdministrator: Thực hiện yêu cầu tạo và lưu báo cáo.
- ReportGenerator: Quản lý tạo báo cáo dựa trên tiêu chí được cung cấp và lưu báo cáo nếu cần.
- ReportCriteriaValidator: Kiểm tra tiêu chí hợp lệ của báo cáo.
- ReportRepository: Lưu hoặc xóa báo cáo tùy yêu cầu.
- ErrorHandler: Hiển thị lỗi khi tiêu chí không hợp lệ hoặc bị thiếu.
      
**Biểu đồ lớp**

![Class Diagram](https://www.planttext.com/api/plantuml/png/V55B2i8m4Dtd55tgmYj8fOWkHS7zqCnYC2PrPbeeuibSU2IlO6Ch3LNC8f1vlxpaUN_aei1QdvsH4_cCWw0f7OXaEsWvEBUoP_8aog21iwl9kiLugL5qZrLWBHX1AVZPFCKEq62FT_ER6JpxoGOzfdPbT1ZPSIH_v0MJ8XCSmP5DR9h-Z1_yMnbteKxH3f8OCoHQTAYOQjRCWRVWhSDFX2Mf7BHlfAV-VAN5OZcjQgRLHyvNdp_SiS5FKdfbawEtyMDV0000__y30000)
- Giải thích biểu đồ lớp trong hệ thống Create Administrative Report:
  + PayrollAdministrator: Lớp đại diện cho quản trị viên, với nhiệm vụ yêu cầu tạo báo cáo và lưu báo cáo.
  + ReportGenerator: Tạo báo cáo dựa trên tiêu chí do PayrollAdministrator cung cấp, kiểm tra tiêu chí qua ReportCriteriaValidator và lưu báo cáo nếu cần.
  + ReportCriteriaValidator: Xác minh tính hợp lệ của tiêu chí báo cáo.
  + ReportRepository: Lưu hoặc xóa báo cáo dựa trên yêu cầu.
  + ErrorHandler: Hiển thị thông báo lỗi khi có thông tin thiếu hoặc không hợp lệ.
# 2. Phân tích ca sử dụng Create Employee Report
**Các lớp phân tích:**

**Biểu đồ sequence**

**Thuộc tính và Quan hệ:**

**Biểu đồ lớp**
# 3. Phân tích ca sử dụng Login
**Các lớp phân tích:**

**Biểu đồ sequence**

**Thuộc tính và Quan hệ:**

**Biểu đồ lớp**
# 4. Phân tích ca sử dụng Maintain Employee Information
**Các lớp phân tích:**

**Biểu đồ sequence**

**Thuộc tính và Quan hệ:**

**Biểu đồ lớp**
# 5. Phân tích ca sử dụng Maintain Purchase Order
**Các lớp phân tích:**

**Biểu đồ sequence**

**Thuộc tính và Quan hệ:**

**Biểu đồ lớp**
# 6. Phân tích ca sử dụng Run Payroll
**Các lớp phân tích:**

**Biểu đồ sequence**

**Thuộc tính và Quan hệ:**

**Biểu đồ lớp**
