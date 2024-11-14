# Lab 3. Identify design elements
Xác định các phần tử thiết kế của hệ thống “Payroll System”
## 1. Subsystem context diagrams
### a. BankSystem
**Biểu đồ ngữ cảnh**

![Context Diagram](https://www.planttext.com/api/plantuml/png/N8yn3i8m34LtdyBg14Clm80AXHq9BX2Lq5HD7PIu4XaH9-4ER1qOUfAUW2lGbY1KrkVtl-rNyqmS2yjrfS6L1Q4rJW8Nh2McXbXU63U5oAsey6GihWMLU-zOLW0Yuvv4E-6jqHe_E4BXCA0W1czRdRNnKeuTkCeoKnEF-dSI6C0aZt6ynDblyHmNU53jWtBa_c1MWXIoQUy44sk8_JNtoLJLlcjkVQxecYi199AEm_Tl0000__y30000)

**Giải thích các thành phần trong biểu đồ**
- **Payroll System:**
Đây là hệ thống quản lý nhân viên, lương và phúc lợi. Payroll System đóng vai trò là hệ thống chính điều khiển việc tính toán lương cho từng nhân viên và gửi thông tin thanh toán cho BankSystem.
- **BankSystem:**
  + Là hệ thống con nhận dữ liệu thanh toán từ Payroll System và thực hiện chuyển tiền vào tài khoản ngân hàng của nhân viên.
  + Thông tin thanh toán từ Payroll System bao gồm chi tiết về số tiền cần trả, ID tài khoản ngân hàng của nhân viên, và các thông tin cần thiết khác cho giao dịch.
- **Employee Bank Account:**
  + Là tài khoản ngân hàng của nhân viên nhận tiền thanh toán từ BankSystem. Mỗi nhân viên có một tài khoản ngân hàng mà BankSystem sẽ thực hiện giao dịch chuyển tiền vào đó.
  + Trong biểu đồ, BankSystem chuyển tiền đến Employee Bank Account khi nhận yêu cầu thanh toán từ Payroll System.


### b. PrintService
**Biểu đồ ngữ cảnh**

![Context Diagram](https://www.planttext.com/api/plantuml/png/N8yn3e9044NxESKFbHPSmCAGo058EC56LzouB6PtC59RM7i4Jw2r53I6U-m9l88GY16xoSjxCvbttKIEXUKor-Jsoi0MJX8hrXAhmh0yCM8bCYjoR0kBn2h3gRH7jPP4OiqT2n9HsK9hf9LZcGSG3YCQoDVhOsa7OPY99YR2S8dPxv4v5eXzVOTMlhwKEEoKVpObTFjeRoQZFxdlnzLTc4nblAw-FaCPeaYQJV_p1m00__y30000)

**Giải thích các thành phần trong biểu đồ**
- **Payroll System:** Gửi dữ liệu phiếu lương cho PrintService, bao gồm các thông tin như tên nhân viên, số giờ làm, và tổng lương.
- **PrintService:**
  + Là hệ thống con nhận dữ liệu phiếu lương từ Payroll System và chuẩn bị các phiếu lương ở dạng có thể in được.
  + PrintService tiếp nhận dữ liệu, định dạng lại thông tin nếu cần, và chuẩn bị phiếu lương để gửi đến máy in.
- **Printer:**
  + Thiết bị in nhận dữ liệu từ PrintService và in phiếu lương. Phiếu lương in ra sẽ được cung cấp cho nhân viên để biết chi tiết về lương và các khoản khấu trừ khác.
  + Trong biểu đồ, PrintService gửi dữ liệu phiếu lương đã chuẩn bị đến Printer.
### c. ProjectManagementDatabase subsystems
**Biểu đồ ngữ cảnh**

![Context Diagram](https://www.planttext.com/api/plantuml/png/V90z2i9048NxFSKZbHPU88K8fXK2LfRZkeRe_i3k99WJU0h1Jh2niJA5HKwI4tW54xInCELylFSzc5Vzd0KcpuNH8knp2--24fopLfWxo-h0I7BAF1bidKVgtKv9Nf2bJ1bbEI6cDNKTGPAxG9HIvPtMM5Q1bOb00L_q8KByd9XCfXZzrOuHOzLS2yZsSIcGvMrzWcxE1cLpXcpkDaFPmQCKGv9-v7SsHjBMD-Y-E-mLCsKt_N_U0000__y30000)

**Giải thích các thành phần trong biểu đồ**
- **Payroll System:**
  + Đóng vai trò là hệ thống điều khiển, yêu cầu thông tin từ ProjectManagementDatabase về giờ làm và chi tiết công việc của nhân viên.
  + Thông tin này được dùng để tính toán lương cho từng nhân viên dựa trên số giờ làm việc và dự án họ tham gia.
- **ProjectManagementDatabase:**
  + Là hệ thống con lưu trữ thông tin dự án và giờ làm của nhân viên. Database này bao gồm thông tin về các dự án đang thực hiện, chi tiết nhiệm vụ, và giờ làm của từng nhân viên.
  + Khi Payroll System yêu cầu, ProjectManagementDatabase trả về dữ liệu giờ làm và chi tiết công việc của từng nhân viên, giúp Payroll System tính toán lương chính xác dựa trên công việc thực tế.

## 2. Analysis class to design element map

**Bảng tóm tắt ánh xạ các lớp phân tích sang các phần tử thiết kế cho hệ thống "Payroll System":**

| **Lớp Phân Tích**            | **Phần Tử Thiết Kế**    | **Mô Tả**                                                                                      |
|------------------------------|-------------------------|------------------------------------------------------------------------------------------------|
| `Employee`                   | EmployeeClass           | Quản lý thông tin và dữ liệu của nhân viên.                                                    |
| `Payroll Administrator`      | PayrollAdminClass       | Quản lý nhân viên, bao gồm các chức năng thêm, xóa, sửa thông tin và tạo báo cáo.              |
| `Timecard`                   | TimecardClass           | Lưu trữ thông tin giờ làm việc của nhân viên theo từng kỳ lương.                               |
| `Project Management Database`| ProjectDBInterface      | Giao tiếp với cơ sở dữ liệu quản lý dự án hiện có.                                             |
| `Payroll System`             | PayrollSystemClass      | Thực hiện tính toán lương, xử lý thanh toán dựa trên dữ liệu từ TimecardClass và EmployeeClass.|

## 3. Design element to owning package map
**Bảng ánh xạ các phần tử thiết kế của hệ thống "Payroll System" vào các gói phù hợp:**

| **Phần Tử Thiết Kế**      | **Gói (Package)**  | **Mô Tả**                                                                           |
|---------------------------|--------------------|-------------------------------------------------------------------------------------|
| `EmployeeClass`           | EmployeeManagement | Gói quản lý các thông tin và dữ liệu nhân viên.                                     |
| `PayrollAdminClass`       | AdminManagement    | Gói quản lý các chức năng của quản trị viên như thêm, xóa, sửa thông tin nhân viên. |
| `TimecardClass`           | TimeTracking       | Gói quản lý thông tin giờ làm của nhân viên trong mỗi kỳ lương.                     |
| `ProjectDBInterface`      | ProjectManagement  | Gói giao tiếp với cơ sở dữ liệu quản lý dự án hiện có.                              |
| `PayrollSystemClass`      | PayrollProcessing  | Gói xử lý các hoạt động liên quan đến tính toán lương và thanh toán.                |
| `BankTransactionInterface`| ExternalServices   | Gói giao tiếp với hệ thống ngân hàng để thực hiện các giao dịch chuyển khoản.       |
| `PrintJobManager`         | ExternalServices   | Gói xử lý tác vụ in phiếu lương cho nhân viên nhận lương qua đường bưu điện.        |

## 4. Architectural layers and their dependencies
 Biểu đồ mô tả các layers trong hệ thống và quan hệ giữa chúng.

