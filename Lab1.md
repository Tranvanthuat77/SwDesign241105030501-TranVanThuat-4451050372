# 1. Phân Tích Kiến Trúc

## Kiến trúc hệ thống đề xuất:
### Kiến trúc phân lớp (Layered Architecture)

- **Presentation Layer (Giao diện)**:  
  Giao diện cho người dùng (Employee, Payroll Administrator) tương tác với hệ thống để thực hiện các tác vụ như chọn phương thức thanh toán, nhập thông tin thời gian làm việc.

- **Business Logic Layer (Xử lý nghiệp vụ)**:  
  Quản lý logic tính toán lương, lưu trữ thông tin thời gian làm việc và xử lý các giao dịch thanh toán.

- **Data Access Layer (Truy cập dữ liệu)**:  
  Xử lý truy xuất dữ liệu từ cơ sở dữ liệu (bao gồm cả DB2 cho quản lý dự án).

### Giải thích lý do lựa chọn kiến trúc:
- **Phân tách rõ ràng trách nhiệm**:  
  Presentation Layer chỉ chịu trách nhiệm hiển thị và thu thập thông tin từ người dùng. Business Logic Layer sẽ xử lý các yêu cầu phức tạp, còn Data Access Layer sẽ làm việc trực tiếp với cơ sở dữ liệu.

- **Dễ bảo trì và mở rộng**:  
  Kiến trúc phân lớp giúp dễ dàng thay đổi từng thành phần riêng lẻ mà không ảnh hưởng đến các phần khác.

![Biểu đồ package](https://www.planttext.com/api/plantuml/png/T95DJiD038NtSmgJ5Lrqmv85QlgZBWXIKBc0DMEY4VCJZLqf8yJ5OD6pS0AkG890e4dnyjdl-PFzyNPQiM2IetVgmj2Z3GHjlRcjzxlBOG4zwYVi20P0XcgebFffjecOWg3O61hCb1Rmh62iH5emT8vWvtiNCr4XjvXJTAustWRBab1YAaOUh2UDoSoTVjofNdunraSUaPcRs5dz3yVtmaBTHEyjyuXFvc_Y5WLhhQVCyt7RzTKXiv0lzBjyk6--aihJm79v0tDIk8PgRp62sFVNKr-fCoEJio2QsTIAWfaU-0a00F__0m00)

---

# 2. Cơ Chế Phân Tích

### Các cơ chế cần giải quyết:
- **Xử lý thời gian và tính lương**:  
  Cơ chế ghi nhận và tính toán thời gian làm việc, số giờ và lương cho từng nhân viên (bao gồm tính cả hoa hồng cho Commissioned Employee).

- **Tích hợp với DB2**:  
  Cơ chế kết nối và đồng bộ thông tin với cơ sở dữ liệu quản lý dự án sử dụng DB2 để quản lý các thông tin liên quan đến các đơn hàng hay các dự án nhân viên đang tham gia.

- **Cơ chế thanh toán**:  
  Hỗ trợ nhiều phương thức thanh toán: tiền mặt, chuyển khoản qua ngân hàng, hoặc thông qua các hệ thống khác.

- **Bảo mật và xác thực**:  
  Cơ chế bảo mật để đảm bảo rằng chỉ có những người dùng đã xác thực mới có thể thực hiện các chức năng như tạo báo cáo hoặc chạy tính lương.

---

# 3. Phân Tích Ca Sử Dụng Payment

### 3.1. Xác định các lớp phân tích
Các lớp phân tích cho ca sử dụng "Select Payment" bao gồm:

- **Employee (Nhân viên)**: Đại diện cho nhân viên tham gia vào quá trình chọn phương thức thanh toán.
- **Payroll System (Hệ thống trả lương)**: Lớp chính điều khiển toàn bộ hệ thống trả lương, bao gồm việc xác nhận và thực hiện việc thanh toán.
- **Payment Method (Phương thức thanh toán)**: Đại diện cho các phương thức thanh toán khác nhau mà nhân viên có thể chọn, như chuyển khoản ngân hàng, tiền mặt, hoặc séc.
- **Bank System (Hệ thống ngân hàng)**: Tương tác với hệ thống để thực hiện việc chuyển tiền nếu phương thức thanh toán là qua ngân hàng.
- **Payment Processor (Bộ xử lý thanh toán)**: Thực hiện việc xử lý thanh toán dựa trên phương thức đã chọn.

### 3.2. Mô tả hành vi qua biểu đồ Sequence
![Sequence](https://www.planttext.com/api/plantuml/png/V9F1IiD048RlUOeX9ptu0XwaA88NfQ07FQxR9LkQp8Pa0-RimODuy0sCHKIXeE0fGJoiz3ts2VeAxgOstJHjJzaTPhx_dt_9hFhffP8aCej2Zr0f4ZYEub3aZ7cnAG_fC2OemU-JF15X2ETvAbda0qdXlpIlTBeZPWwdJ78nM7JRqhpIxZuaE7B1zhwDsay4PMag4XVS53rliG7i7RHDmZxuHrnN3mWndtvC2mn0cliRDH-27AHG1VfUUsXEMPgtb9EXhcwn7hu7gWgw2lHNNRJdDxZOEGlKCm9NJnZirZwSiNNRN5ffvBgST66_ZseCj1RQl58JcwLTgVSCg2vVCxZHrGH2zTq9fZraGClNieWBe_T9WPjyxj2ePtaTr8WBNOuDmUdUOC9ToH4tPvCADs5_OR3UoTPqN5IT31U61rANBt9DFCthrJjPJRXMXTZYgCTmOF-YFm000F__0m00)

### 3.3. Nhiệm vụ của từng lớp phân tích
- **Employee**: Chọn và xác nhận phương thức thanh toán.
- **Payroll System**: Điều phối toàn bộ quy trình từ nhận thông tin đến giao tiếp với các lớp khác.
- **Payment Method**: Lưu trữ thông tin về các phương thức thanh toán và nhận lựa chọn của nhân viên.
- **Bank System**: Thực hiện việc chuyển khoản cho nhân viên khi được yêu cầu.
- **Payment Processor**: Xử lý thanh toán qua các phương thức khác nhau.

### 3.4. Thuộc tính và quan hệ giữa các lớp
- **Employee**: Có thuộc tính như employeeId, name, selectedPaymentMethod.
- **Payment Method**: Bao gồm thuộc tính như paymentType, accountDetails.
- **Payroll System**: Liên kết với Payment Method và Employee, điều phối việc chọn phương thức thanh toán và lưu trữ thông tin.
- **Bank System**: Liên kết với Payroll System để xử lý việc chuyển khoản.

---

# 4. Phân Tích Ca Sử Dụng Maintain Timecard

### 4.1. Xác định các lớp phân tích
Các lớp phân tích cho ca sử dụng "Maintain Timecard" bao gồm:

- **Employee (Nhân viên)**: Nhân viên sẽ nhập thông tin thời gian làm việc.
- **Timecard (Bảng chấm công)**: Đại diện cho thông tin về thời gian làm việc của nhân viên.
- **Payroll System (Hệ thống trả lương)**: Quản lý và lưu trữ thông tin thời gian làm việc, sau đó sử dụng để tính lương.
- **Project Database (Cơ sở dữ liệu dự án)**: Lưu trữ thông tin liên quan đến các dự án mà nhân viên tham gia, cần thiết để tính toán lương dựa trên các nhiệm vụ đã hoàn thành.

### 4.2. Mô tả hành vi qua biểu đồ Sequence
![Sequence](https://www.planttext.com/api/plantuml/png/V9B1IiGm443l-Ohv0N-W1rbGmOE2u1wypgPX6qZIqiuAFU_1WmZ-WB15zY8ihE2fFNZeql_85_WBJhiKhRisa4EIcJSlatnLdvECCAM5DG8bnIbSsCJ4kL8YuMqjTOAEu0RpD3RcDiz8sS79EHBEC5D2z8bmSZgC3s3tl5kwERZ8bvj430xRw9uHm5rTIA38L-_oHsG4VCQXJmwkKJlY2LDjbSGq7AjnvSjr3ZDVlhAIPAMr1Lb_y2BIldfmGBuiz26XrmZWakEMhlDyF0OQDMvRiEy4TOGN3NED3aozid3V6iXH-sQxuBpEb_Z6yXTF23G4qthZ8g2uBXZQR9k2XO370VIFsP4y2Fab42Yjtzo_iig5OgnRtPjsWaFRzXOhhhXlsOGnxIVy1W00__y30000)

### 4.3. Nhiệm vụ của từng lớp phân tích
- **Employee**: Nhập và cập nhật thông tin thời gian làm việc.
- **Timecard**: Lưu trữ thông tin về thời gian làm việc của nhân viên.
- **Payroll System**: Quản lý và lưu trữ thông tin thời gian làm việc, sử dụng dữ liệu từ Timecard để tính toán lương.
- **Project Database**: Cung cấp thông tin về dự án liên quan đến các nhiệm vụ mà nhân viên thực hiện.

### 4.4. Thuộc tính và quan hệ giữa các lớp
- **Employee**: Có thuộc tính như employeeId, name, timecard.
- **Timecard**: Có thuộc tính như workingHours, date, projectDetails.
- **Payroll System**: Liên kết với Timecard và Project Database để tính toán lương dựa trên thông tin nhập từ nhân viên.
- **Project Database**: Lưu trữ các thông tin dự án và liên kết với Payroll System.

---

# 5. Hợp Nhất Kết Quả Phân Tích

### 5.1 Tổng Quan về Hệ Thống "Payroll System"
Hệ thống "Payroll System" được xây dựng nhằm mục đích tối ưu hóa quy trình tính toán và thanh toán lương cho nhân viên tại Acme, Inc. Hệ thống cho phép nhân viên ghi lại thời gian làm việc và lựa chọn phương thức thanh toán một cách linh hoạt. Qua phân tích, chúng tôi đã xác định hai ca sử dụng chính: Select Payment và Maintain Timecard.

### 5.2 Phân Tích Ca Sử Dụng "Select Payment"
**Mục Đích**: Ca sử dụng này cho phép nhân viên lựa chọn phương thức thanh toán phù hợp với nhu cầu của họ.

**Các Lớp Phân Tích**:
- **Employee**: Đại diện cho nhân viên thực hiện việc chọn phương thức thanh toán.
- **Payroll System**: Lớp chính điều phối toàn bộ quy trình thanh toán.
- **Payment Method**: Lưu trữ thông tin về các phương thức thanh toán như chuyển khoản ngân hàng, tiền mặt.
- **Bank System**: Thực hiện chuyển khoản cho nhân viên nếu phương thức thanh toán là qua ngân hàng.
- **Payment Processor**: Chịu trách nhiệm xử lý thanh toán qua các phương thức khác nhau.

**Biểu Đồ Sequence**: Mô tả quy trình từ khi nhân viên chọn phương thức thanh toán cho đến khi xác nhận thanh toán thành công.

### 5.3 Phân Tích Ca Sử Dụng "Maintain Timecard"
**Mục Đích**: Ca sử dụng này cho phép nhân viên nhập và cập nhật thông tin thời gian làm việc của họ.

**Các Lớp Phân Tích**:
- **Employee**: Nhân viên nhập và cập nhật thông tin về thời gian làm việc.
- **Timecard**: Lưu trữ thông tin chi tiết về thời gian làm việc của nhân viên.
- **Payroll System**: Quản lý và lưu trữ thông tin thời gian làm việc, sử dụng để tính toán lương.
- **Project Database**: Cung cấp thông tin về các dự án mà nhân viên tham gia, cần thiết cho việc tính lương.

**Biểu Đồ Sequence**: Mô tả quy trình từ khi nhân viên nhập thông tin thời gian cho đến khi hệ thống tính toán lương dựa trên thông tin từ Timecard.

### 5.4 Kết Luận
Việc phân tích hai ca sử dụng "Select Payment" và "Maintain Timecard" cho thấy cách mà hệ thống "Payroll System" hoạt động một cách hiệu quả. Kiến trúc phân lớp không chỉ giúp tách biệt rõ ràng các trách nhiệm của từng thành phần mà còn tạo điều kiện thuận lợi cho việc bảo trì và mở rộng hệ thống trong tương lai. Qua đó, hệ thống có khả năng đáp ứng tốt hơn các yêu cầu của người dùng và nâng cao trải nghiệm sử dụng.





