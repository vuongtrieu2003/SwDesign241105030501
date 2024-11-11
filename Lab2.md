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
- Giải thích biểu đồ lớp:
  + PayrollAdministrator: Lớp đại diện cho quản trị viên, với nhiệm vụ yêu cầu tạo báo cáo và lưu báo cáo.
  + ReportGenerator: Tạo báo cáo dựa trên tiêu chí do PayrollAdministrator cung cấp, kiểm tra tiêu chí qua ReportCriteriaValidator và lưu báo cáo nếu cần.
  + ReportCriteriaValidator: Xác minh tính hợp lệ của tiêu chí báo cáo.
  + ReportRepository: Lưu hoặc xóa báo cáo dựa trên yêu cầu.
  + ErrorHandler: Hiển thị thông báo lỗi khi có thông tin thiếu hoặc không hợp lệ.
# 2. Phân tích ca sử dụng Create Employee Report
**Các lớp phân tích:**
- Employee: Người dùng yêu cầu tạo báo cáo.
- ReportGenerator: Xử lý yêu cầu tạo báo cáo dựa trên các tiêu chí được cung cấp.
- ReportCriteriaValidator: Kiểm tra tiêu chí báo cáo có hợp lệ không.
- ReportRepository: Lưu hoặc loại bỏ báo cáo theo yêu cầu.

**Biểu đồ sequence**

![Sequence Diagram](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3bTnTcQUGb5-SIfNOd99Vf62Qsv1JdvbQYeNZA6WQwSGb5gGNrJYdfgNMfG8L6Ib47buLQb2yiDToqiLIXxkMfYla7GOI2G32IuqjGZjpaMP9Qb5cObXYJcPAH1Z8WulJ5OeoNYuUoEGoWIRcN5uBOPX63gnkYa4OG3GnCK52ZaFTxVZTWwoJi9UW8M6bO97viFTpNbWLtSZwI4sk7AERIWbrYhaK3wyAa-XxF02XJAGjIL5G4-2JC9lhNDfNZf8_z82BFfnXmo8BCu42bLQAVXWSov2WO8kDdkTOEeLZamyl1ZYK8VKl1HGUWC0003__mC0)

**Thuộc tính và Quan hệ:**
- Employee: Yêu cầu tạo và lưu báo cáo.
- ReportGenerator: Xử lý tạo báo cáo và yêu cầu lưu báo cáo.
- ReportCriteriaValidator: Kiểm tra tiêu chí báo cáo.
- ReportRepository: Lưu hoặc xóa báo cáo.

**Biểu đồ lớp**

![Class Diagram](https://www.planttext.com/api/plantuml/png/V51B2i8m4Dtd55tgebUGGX7t2kv3-nR1DAapqq8HJ-R28ta56n9jQQ5P1F9-yoQVrxjWqIHTOnNVZCl8CrHbDNDsR5hh1o1xg6myX7i7bZDQJr8Ij1ZlTlivTz4z8Z_YJvLo8dA20sdnbEAga32f0yGRzfACW8o-QclgMKmVt_ZnQsUusOoE8Ld2c3InXeKWUlxhvlbXsLajTvWqgs8RsgcAAk3gyEbV0000__y30000)
- Giải thích biểu đồ lớp:
  + Employee: Lớp đại diện cho nhân viên yêu cầu tạo báo cáo và lưu báo cáo.
  + ReportGenerator: Xử lý việc tạo báo cáo theo yêu cầu của nhân viên. Lớp này kiểm tra tiêu chí qua ReportCriteriaValidator và tương tác với ReportRepository để     lưu báo cáo nếu cần.
  + ReportCriteriaValidator: Xác minh tính hợp lệ của tiêu chí báo cáo như loại báo cáo, ngày tháng và tên nhân viên.
  + ReportRepository: Lưu trữ hoặc xóa báo cáo dựa trên yêu cầu.
# 3. Phân tích ca sử dụng Login
**Các lớp phân tích:**
- User: Người dùng nhập thông tin đăng nhập.
- LoginService: Xử lý xác thực thông tin đăng nhập.
- UserRepository: Kiểm tra thông tin từ cơ sở dữ liệu để xác thực đăng nhập.

**Biểu đồ sequence**

![Sequence Diagram](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3bTnTcQUGb5-SIfNOd99Vf52Q75g4HU8KD2rK_39Jy_C2qujAijCJhLIyCjuk6jjWKB9uLLv2aSc7cdEIrV8WmYL7LwWa0jabIXa0mLMbd8XQmGP138mABKWlpWJQ4UbbO9tviFTpRaA9KM92YKPXxS0JIh9H3EK2rMFWYw6Uq8GEZCUxbvSe93pS7SxLgkj58vCG7OlqCu5UHaAoI3zN0wfUIcWa000003__mC0)

**Thuộc tính và Quan hệ:**
- User: Cung cấp thông tin đăng nhập.
- LoginService: Xác thực thông tin và thông báo kết quả đăng nhập.
- UserRepository: Kiểm tra thông tin từ cơ sở dữ liệu.

**Biểu đồ lớp**

![Class Diagram](https://www.planttext.com/api/plantuml/png/R9112i9034NtSufPLh0Nw48ARbrPFC0u3UtGQLAIQKN4axdmI5x1JgdYW5c5d-Jb9w_7ivHWE8ozLz8vr4m2odeZeay2h6zApp7EAPeU2bq5TjWiuZ0tNOZhHFJKECmswgvMoY4A5V3aBAmqCuOMC3Xh0cGVzFRB-ncE5eumaBX0V5t7RGksspFKaM6y_4CK-apamM1aBOVa-IxneX9ZiPekKoLW7T_o1W00__y30000)
- Giải thích biểu đồ lớp:
  + User: Đại diện cho người dùng nhập thông tin đăng nhập (tên người dùng và mật khẩu) và yêu cầu đăng nhập.
  + LoginService: Xác thực thông tin đăng nhập của người dùng. Dịch vụ này gọi UserRepository để kiểm tra thông tin.
  + UserRepository: Kiểm tra thông tin đăng nhập từ cơ sở dữ liệu và phản hồi kết quả cho LoginService.
# 4. Phân tích ca sử dụng Maintain Employee Information
**Các lớp phân tích:**
- PayrollAdministrator: Người thực hiện thêm, cập nhật hoặc xóa thông tin nhân viên.
- EmployeeService: Xử lý các thao tác thêm, sửa hoặc xóa nhân viên.
- EmployeeRepository: Lưu trữ và truy xuất thông tin nhân viên.

**Biểu đồ sequence**

![Sequence Diagram](https://www.planttext.com/api/plantuml/png/Z94n2i8m58RtdE9Tm0jqa8e83WwYasD8WmscIKbU2hsD2Y9qSd3ImI7WFJo1Lp0T15iZk3r-tl-z3zxpUaijKeEkaCHkX0AZBIUKeJOmfxNHKewoGYXXqT0GabW8Wo5CYbBgclCbDvLWF86LRnomn-Ne07Eg0VsE0HhVA52vtokeH9X9hzUYOYTwF7zMQq3HHVsjDdQX7L27yWCLCtb72rvgAmAkJc1sF_qq-Dw7GKnWglrM0GO31DdbaPIhhFt62m00__y30000)

**Thuộc tính và Quan hệ:**
- PayrollAdministrator: Thực hiện thao tác quản lý thông tin nhân viên.
- EmployeeService: Điều phối quá trình xử lý thông tin nhân viên.
- EmployeeRepository: Lưu hoặc cập nhật thông tin của nhân viên trong cơ sở dữ liệu.

**Biểu đồ lớp**

![Class Diagram](https://www.planttext.com/api/plantuml/png/Z90n3i8m34Ltdo8Z3Bq2AWC36u8JM8r14KvInMcb274o1ex45KYbL41WmEFp_r_-VjpkhKGCSR0CSZPE1Iy47QE8sc4AddcjhN56Oi3eWxg0ocFHuOasjcUVYBRkw1TBk48npln0OJGT5GzgFI-oU293hp5I1JKnVS2ls3trNam-9fLamR5E-JlwPyccMTKbe2xrhdbT12qvFJtp2G00__y30000)
- Giải thích biểu đồ lớp:
  + PayrollAdministrator: Quản trị viên thực hiện các thao tác thêm, cập nhật hoặc xóa thông tin nhân viên.
  + EmployeeService: Điều phối các yêu cầu xử lý thông tin nhân viên, gồm thêm, cập nhật và xóa thông tin.
  + EmployeeRepository: Lưu, cập nhật, hoặc xóa dữ liệu nhân viên trong cơ sở dữ liệu.
# 5. Phân tích ca sử dụng Maintain Purchase Order
**Các lớp phân tích:**
- CommissionedEmployee: Nhân viên bán hàng ghi nhận đơn đặt hàng.
- PurchaseOrderService: Xử lý các thao tác thêm, sửa, xóa đơn đặt hàng.
- PurchaseOrderRepository: Lưu trữ thông tin đơn đặt hàng.

**Biểu đồ sequence**

![Sequence Diagram](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3bTnTcQUGb5-SIfNOd99Vf62StvkRcPnSMP-NcgAQsv1JdvbQYeNDa45NJk5WDAYv8p4ubJ_efJKek3KehBCv5Gh1UUCXxjxynHACXBp5KeEBqnMA2awl2fFuSZ4Omj1vCDTsqiKCWulo4ldmgOVP2us-wmK8W-lAbL8VhXhUIdGxCDRyj8LIZ9XnaBC8z6TfK0ZWEOjBS1b7YxteOW7fHRa5sS2mwxIIi7ds0QSZiEXIK4NfmCzye4Q5Kg0BYnHo06PZ6oSGsfU2YW20G000F__0m00)

**Thuộc tính và Quan hệ:**
- CommissionedEmployee: Thực hiện các thao tác với đơn đặt hàng.
- PurchaseOrderService: Xử lý thêm, sửa, xóa đơn hàng.
- PurchaseOrderRepository: Lưu và quản lý thông tin đơn đặt hàng trong hệ thống.

**Biểu đồ lớp**

![Class Diagram](https://www.planttext.com/api/plantuml/png/b91D2i9038NtESKiTT4hY22k5Jr1c7deuFoKP5eeuibSU2Ile8Mgg0KnovTyZ_ToFL_cMbXA4mFfmISZMK4siAfPv1Yzgiy9RXdha3l07CdS9tBY7TQDs3qhLk8WaocTQ23V5bj8w-s3j08kJw9NcjfzA0u1vOVh1dLMNx9qWx5o-w_jQC6gcetcfz5INzUlN3H7SlrVRm000F__0m00)
- Giải thích biểu đồ lớp:
  + CommissionedEmployee: Nhân viên thực hiện các thao tác với đơn đặt hàng.
  + PurchaseOrderService: Xử lý việc thêm, cập nhật, và xóa đơn đặt hàng của nhân viên.
  + PurchaseOrderRepository: Lưu trữ thông tin đơn đặt hàng mới hoặc cập nhật thông tin đơn đặt hàng trong cơ sở dữ liệu.
# 6. Phân tích ca sử dụng Run Payroll
**Các lớp phân tích:**
- PayrollScheduler: Kích hoạt quá trình chạy bảng lương vào ngày định kỳ.
- PayrollProcessor: Xử lý bảng lương cho từng nhân viên.
- EmployeeRepository: Cung cấp thông tin nhân viên để tính lương.
- PaymentService: Quản lý phương thức thanh toán và xử lý trả lương.
- BankSystem: Xử lý giao dịch ngân hàng đối với thanh toán chuyển khoản.

**Biểu đồ sequence**

![Sequence Diagram](https://www.planttext.com/api/plantuml/png/Z9B1IWCn48Rl-nJp0ds17gG71KKFnNhmkcR39dGtAKcsk6UFNdm1eLMAQ2bu48HTf8T8toDFu2iuqMsjQoYUCeIPR_v_PZxgPK-RM9aYpo8zv0AKr3IAYP4A1gKsD8--7-ZiGJykbSoo0M4qAJAgkl1-uwgb0CDSVSiXvJ76obNtaAsULrEHHkqIZpd8HvaiAJsb8wavTYgxSEAgMGb9B1XeEoKC1BDt0iRSFWaWhdfeW_z2e1EKk1za1eKrVtqb2TLQOl6vgnUGsJUumDuYNNS7mYGOLyyn340tWDrk3RCl230uzMt8RcTRuix2zI4H-9TJOGPKZJcXM6eNE9Mrcx6Tm92Xfi8FkPv7lzD3W6FkwgiSqsCOiGRZh-2HuECdRgITYd-0ZWG2E5vHiP73fAjU2QGu-w-Raf2u-jhlB_KkcPty75RRPMlvXnAJSLFLpC1biykeHqNYx_qJ003__mC0)

**Thuộc tính và Quan hệ:**
- PayrollScheduler: Tự động khởi chạy quá trình trả lương vào thời gian đã định.
- PayrollProcessor: Tính lương cho từng nhân viên và áp dụng các khấu trừ cần thiết.
- EmployeeRepository: Cung cấp thông tin nhân viên cho quy trình tính lương.
- PaymentService: Xử lý thanh toán theo phương thức mong muốn của nhân viên.
- BankSystem: Xử lý giao dịch ngân hàng nếu thanh toán qua chuyển khoản.

**Biểu đồ lớp**

![Class Diagram](https://www.planttext.com/api/plantuml/png/R9712i8m38RlUOeUzR1N416y3-SBb2veMTkCf1EA-6GUV2HVGSSsTEjw2_-ND1zvFrzxYPfZvnr8OuDY4WJZj8WgTM9ohZ9Nh3k7hEwWle-xC2QRBJnW3fTC1aLeWjkXNcau-jPHGZnXIs8ZSHfRBXYdJ1O_U0onGhvPWzdyFll73peqLPA8VewUMGVH9beA0vvf5iKkqu7ChwToXtLklZeiJ7hYjotiCTJzEJu0003__mC0)
- Giải thích biểu đồ lớp trong hệ thống Run Payroll:
  + PayrollScheduler: Kích hoạt quá trình chạy bảng lương tự động vào ngày định kỳ.
  + PayrollProcessor: Tính lương cho từng nhân viên và xử lý các khoản khấu trừ.
  + EmployeeRepository: Cung cấp thông tin nhân viên để tính lương.
  + PaymentService: Xử lý các hình thức thanh toán và in phiếu lương hoặc gửi giao dịch ngân hàng.
  + BankSystem: Xử lý giao dịch ngân hàng nếu nhân viên chọn phương thức chuyển khoản.
# 7. Viết code Java mô phỏng ca sử dụng Maintain Timecard.
package Thietkephanmem;

import java.util.*;

class Employee {
    private String name;
    private String id;

    public Employee(String name, String id) {
        this.name = name;
        this.id = id;
    }

    public String getId() {
        return id;
    }
}

class Timecard {
    private String employeeId;
    private Map<String, Integer> hoursWorked; // chargeNumber -> số giờ làm việc
    private boolean submitted;
    private Date startDate;
    private Date endDate;
    private Date submittedDate;

    public Timecard(String employeeId, Date startDate, Date endDate) {
        this.employeeId = employeeId;
        this.startDate = startDate;
        this.endDate = endDate;
        this.hoursWorked = new HashMap<>();
        this.submitted = false;
    }

    // Thêm giờ làm việc vào timecard
    public void addHours(String chargeNumber, int hours) {
        if (hours < 0 || hours > 24) {
            throw new IllegalArgumentException("Giờ làm không hợp lệ. Phải nằm trong khoảng từ 0 đến 24.");
        }
        hoursWorked.put(chargeNumber, hours);
        System.out.println("Đã thêm " + hours + " giờ cho mã " + chargeNumber);
    }

    // Gửi timecard
    public void submit() {
        if (submitted) {
            System.out.println("Timecard đã được gửi. Không thể chỉnh sửa.");
            return;
        }
        submittedDate = new Date();
        submitted = true;
        System.out.println("Timecard đã được gửi thành công vào ngày: " + submittedDate);
    }

    // Kiểm tra xem timecard đã được gửi hay chưa
    public boolean isSubmitted() {
        return submitted;
    }

    // Hiển thị thông tin giờ làm việc
    public void displayHours() {
        System.out.println("Giờ làm việc trên Timecard:");
        for (Map.Entry<String, Integer> entry : hoursWorked.entrySet()) {
            System.out.println("Mã: " + entry.getKey() + ", Giờ: " + entry.getValue());
        }
    }
}

class MaintainTimecardService {
    private List<String> availableChargeNumbers;

    public MaintainTimecardService() {
        // Danh sách mã dự án (charge numbers) có sẵn để chọn
        availableChargeNumbers = Arrays.asList("A", "B", "C");
    }

    public void processTimecard(Employee employee, Timecard timecard) {
        if (timecard.isSubmitted()) {
            System.out.println("Timecard đã được gửi. Chế độ xem chỉ đọc.");
            timecard.displayHours();
            return;
        }

        System.out.println("Bắt đầu nhập giờ làm cho nhân viên " + employee.getId());
        System.out.println("Danh sách mã dự án có sẵn: " + availableChargeNumbers);

        Scanner scanner = new Scanner(System.in);
        while (true) {
            System.out.print("Nhập mã dự án (hoặc nhập 'xong' để hoàn thành): ");
            String chargeNumber = scanner.nextLine();
            if (chargeNumber.equalsIgnoreCase("xong")) {
                break;
            }
            if (!availableChargeNumbers.contains(chargeNumber)) {
                System.out.println("Mã dự án không hợp lệ.");
                continue;
            }

            System.out.print("Nhập số giờ làm: ");
            int hours = scanner.nextInt();
            scanner.nextLine(); // Đọc bỏ dòng mới

            try {
                timecard.addHours(chargeNumber, hours);
            } catch (IllegalArgumentException e) {
                System.out.println(e.getMessage());
            }
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Employee employee = new Employee("Nguyễn Văn A", "001");
        
        // Giả sử thời gian kỳ làm việc từ hôm nay đến 7 ngày sau
        Date startDate = new Date();
        Calendar calendar = Calendar.getInstance();
        calendar.setTime(startDate);
        calendar.add(Calendar.DAY_OF_YEAR, 7);
        Date endDate = calendar.getTime();

        Timecard timecard = new Timecard(employee.getId(), startDate, endDate);
        MaintainTimecardService service = new MaintainTimecardService();

        service.processTimecard(employee, timecard);

        System.out.print("Bạn có muốn gửi timecard không? (y/n): ");
        Scanner scanner = new Scanner(System.in);
        String choice = scanner.nextLine();

        if (choice.equalsIgnoreCase("y")) {
            timecard.submit();
        } else {
            System.out.println("Bạn chưa gửi timecard. Thay đổi đã được lưu.");
        }

        System.out.println("Kết thúc chương trình.");
    }
}

