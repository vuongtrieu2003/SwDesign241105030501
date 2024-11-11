# 1. Phân tích ca sử dụng Create Administrative Report
**Các lớp phân tích:**
- PayrollAdministrator: Người yêu cầu tạo báo cáo.
- ReportGenerator: Chịu trách nhiệm tạo báo cáo.
- ReportCriteriaValidator: Xác minh tiêu chí báo cáo.
- ReportRepository: Lưu trữ báo cáo.
- ErrorHandler: Hiển thị lỗi.
  
**Biểu đồ sequence**

![Sequence Diagram](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3bTnTcQUGb5-SIfNOd99Vf52G69bKNvEZcDARcPUPd59KI9Ga0kRe8AkdK9GQa5-KObxQbugMCXA8VBmgbA5v8UxbfSgb3pSjJ1V8Uama4W64bneQX7QdOioIrABCXF34dCoKo36H1nUcAnGal5mzqOWbGasC-FmMWp3C7HYTLC8mW2WYOiB578Uxcx7xHnadOIzW2rah1GyCX_kRiu3-w0RIJyvmPXpR4CfEKv0Zed3g_8KoWulK2W3EQUa21WG85E9TuvpQLuwoAob1LZCmXsI8B8u4oXKQQNWWyqR20KAkjZiTOAfLpWoyV1YYACTKlDIGEaM0000__y30000)

**Thuộc tính và Quan hệ:**

- PayrollAdministrator: Có thuộc tính adminId, name, và phương thức generateAdminReport().
- Report: Có thuộc tính reportType, dateRange, content, chứa nội dung của báo cáo.
- System: Liên kết giữa PayrollAdministrator và Report để tạo báo cáo theo tiêu chí.

      
**Biểu đồ lớp**

![Class Diagram](https://www.planttext.com/api/plantuml/png/R90z3i8m38NtdC8Z7Ng130Wa5ZPKk43KMbL4wo377Ih4OPYGE08C39oa9-0AD6rQ2OdDVlRx_FDvlbPU34jJLyeVBG4xZoglZFUmCosxgbeNjINhXOquXhC201EaRQ71aeISJ8qQziAMof2NIDYtus3DyEHO5ecwg0WUbH75GtneJp-0eZTdXifUt4nXq7D7WYHpwupSjrwm7f7Jz3WuPol8raocHCS5WlllZMcwd80QslUzWRnxt1eLjL2E9sYGxd5rQeLKX1T-0G00__y30000)
- Giải thích biểu đồ lớp trong hệ thống Create Administrative Report:
  + Lớp PayrollAdministrator đại diện cho người quản lý hệ thống bảng lương, có thể yêu cầu tạo báo cáo hành chính với các tiêu chí như loại báo cáo (tổng giờ làm hoặc lương), khoảng thời gian, và nhân viên cụ thể.
  + Lớp Report là đối tượng chứa nội dung của báo cáo, có các thuộc tính reportType để lưu loại báo cáo và dateRange để chỉ định khoảng thời gian.
  + Lớp System xử lý yêu cầu từ PayrollAdministrator và tạo Report với dữ liệu phù hợp.
- Quan hệ:
  + PayrollAdministrator gửi yêu cầu tạo báo cáo đến System.
  + System tạo một đối tượng Report và trả lại cho PayrollAdministrator.
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
