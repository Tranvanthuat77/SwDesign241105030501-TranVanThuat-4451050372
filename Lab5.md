1. Hệ thống con: Quản lý Đăng nhập
Mô tả: Chức năng chính: Đảm bảo việc đăng nhập của nhân viên và quản lý vào hệ thống.

Thành phần chính:

Giao diện người dùng: Form đăng nhập, với các trường nhập tên đăng nhập và mật khẩu.
Xử lý Đăng nhập:
Kiểm tra tên đăng nhập và mật khẩu.
Mã hóa mật khẩu (sử dụng thuật toán như bcrypt hoặc PBKDF2).
Kiểm tra quyền truy cập: xác định quyền hạn người dùng (nhân viên hoặc quản lý).
Xác thực: Sử dụng cơ chế xác thực như JWT (JSON Web Token) hoặc OAuth để đảm bảo an toàn.
Quản lý phiên làm việc:
Tạo phiên làm việc khi người dùng đăng nhập thành công.
Duy trì phiên làm việc với cơ chế session hoặc token.
Kiểm tra thời gian hết hạn của phiên làm việc, yêu cầu người dùng đăng nhập lại khi phiên hết hạn.

![subsystem diagram](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3bT1Od9sOdggWb9WwSDTY_CKSWxlLJWouKXpNhf2NiR3NMiBb1IgkHGKadCIYuiLbDpoYt8LZan4baP8HZpSlHQNVWK5NGNlp8UxctCLIeeI5KeEhyf3DKUXxF02XLmWgqGX6oYmiXIgoVVmOeMCmviJiSaX6LXOMlbmTsCUa5rQgP0CCX2efXRXDYJV5MHaWcpFERmWLw4CQ49xCiA98GztBSp7eW8gxG8qlAJey1hiAcgvQhaSKlDIGC4A0000__y30000)

2. Hệ thống con: Quản lý Thời gian làm việc
Mô tả: Chức năng chính: Nhập, lưu trữ và phê duyệt thời gian làm việc của nhân viên.

Thành phần chính:

Giao diện người dùng:
Form nhập thời gian làm việc, cho phép nhân viên nhập số giờ làm việc hàng ngày.
Form phê duyệt thời gian làm việc, cho phép quản lý xem và phê duyệt thời gian làm việc của nhân viên.
Xử lý Thời gian làm việc:
Kiểm tra tính hợp lệ của dữ liệu nhập (ví dụ: giờ làm không được vượt quá số giờ tối đa trong ngày).
Lưu trữ thông tin thời gian làm việc trong cơ sở dữ liệu.
Tính toán thời gian làm việc, bao gồm giờ làm ngoài giờ nếu có.
Quản lý Phê duyệt:
Quản lý xem xét và phê duyệt thời gian làm việc của nhân viên.
Cập nhật trạng thái "đã phê duyệt" hoặc "không phê duyệt" cho từng mục thời gian làm việc.


![subsystem diagram](https://www.planttext.com/api/plantuml/png/X90n2i9044NxdEAJNho2bOqM2XQsImp9OdODoKGKIMLXxG44mKebQ67b8XOBtcDFu1LSHNIniHpc_PatSrVNHauieq8aNig28Oj2-Dt2d3SIYRwW5nkrueWuUzPhWJ4tQX7uc7b0aB0yXzySPG8oDkSg1Nrv_qlqZQh-ZmDgQDbwBa0P0-bAnh21JOh4Kc-YVJiMjc_KmIxJ9nc1kBIzyaSeZVKEWs9ga-IeEBTrNE9Zq0y59dfBxYckwnjpmtKoQe_0yal-CYczHYW7pvy-0000__y30000)

3. Hệ thống con: Quản lý Tiền lương
Mô tả: Chức năng chính: Tính toán và phát hành tiền lương cho nhân viên.

Thành phần chính:

Xử lý Tính lương:
Tính toán tiền lương dựa trên thời gian làm việc và hợp đồng lao động.
Cập nhật các khoản khấu trừ như thuế thu nhập cá nhân, bảo hiểm xã hội, v.v.
Tính lương ngoài giờ và các phụ cấp khác (nếu có).
Phát hành Phiếu lương:
Chuẩn bị phiếu lương cho từng nhân viên, bao gồm thông tin chi tiết như lương cơ bản, phụ cấp, khấu trừ, tổng lương.
Cung cấp phiếu lương dưới dạng PDF hoặc in ra.
Giao dịch Trả lương:
Thực hiện giao dịch trả lương qua ngân hàng (chuyển khoản trực tiếp vào tài khoản nhân viên).
Xác nhận và ghi lại các giao dịch trả lương trong hệ thống.

![subsystem diagram](https://www.planttext.com/api/plantuml/png/Z94nQiD044LxdUAZFdSmf73hW8kq6zdiYiXZ8Qq2mRX8vSALSMsmOaA8mP10AYr1nGRVOqwGAsHa6un88Ec6vR_z_yzykRgJMvNPOfG4gOfkbHuYl2gusX0I_u5-pEv1nlthlYGTOX80KQBo7E4rkzrHutTasXBWulHinxua3DYzATZCRmbQlbm9k1xXJiPPz8VUiDka-5omMv8MxVGSeMTyQM7yMi2UYRcgYvyvBetKUI7Si9l36lzE6ZOcf6tWfEvAgxXng-g3zKmGTWjX1E7gYTe9kh4QDsddaK4_axNztr-VqPRtlTyMYBXwBdwDGTe_qg7pSHdJe3EaGNE_Rm000F__0m00)

4. Hệ thống con: Quản lý Người dùng
Mô tả: Chức năng chính: Quản lý thông tin nhân viên và quản lý.

Thành phần chính:

Giao diện người dùng:
Form thông tin người dùng, cho phép hiển thị và chỉnh sửa thông tin của nhân viên và quản lý.
Xử lý Thông tin người dùng:
Cập nhật thông tin nhân viên (như tên, địa chỉ, số điện thoại, vị trí công việc).
Cập nhật quyền hạn người dùng (ví dụ: quyền xem báo cáo, quyền phê duyệt thời gian làm việc, v.v.).
Lưu trữ thông tin người dùng trong cơ sở dữ liệu.

![subsystem diagram](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3bT1Od9sOdggWb9WwSDTY_CKSWxlLV1BFxRXuUwvcGefXtVcfIifL7CfA2Jd91ONAoYvvHVbAfHa7DwIbwvGafcda8Ug5A4muk7kjM33Gd0g1fkheA2huFnmrze2XRmC85M2P3XKrkVOXbA5agA7kzUZojLorN8vfEQbW7m10000__y30000)

5. Hệ thống con: Quản lý Hệ thống
Mô tả: Chức năng chính: Giám sát và quản lý các chức năng của hệ thống.

Thành phần chính:

Giám sát Hoạt động Hệ thống:
Theo dõi và ghi lại các hoạt động của hệ thống như đăng nhập, thay đổi dữ liệu, giao dịch trả lương.
Cung cấp các báo cáo giám sát hệ thống (ví dụ: báo cáo truy cập, báo cáo lỗi hệ thống).
Quản lý Bảo mật:
Đảm bảo tính bảo mật của hệ thống, thực hiện kiểm tra và cập nhật các chính sách bảo mật.
Áp dụng các biện pháp bảo mật như mã hóa dữ liệu, xác thực người dùng, bảo vệ chống tấn công SQL injection.
Quản lý Sao lưu và Khôi phục:
Thực hiện sao lưu định kỳ cơ sở dữ liệu và các dữ liệu quan trọng.
Cung cấp chức năng khôi phục dữ liệu khi hệ thống gặp sự cố hoặc mất mát dữ liệu.

![subsystem diagram](https://www.planttext.com/api/plantuml/png/R96nJiCm48RtFCMlxBn31KChTQhW1OmJnLOT9sgSBbKdXWvC7H1YeqAC5PM09HPYCE8zxWbu1IweDAsKoVRTV_g-at_yvw1oOkRgt4Iba5EHfOWdDJLF5YPyO4H-1QV8hsqMOn41qeYgGZpKOPEZ2Xk7KK4D7rzhyWyswna1pd2bqW99UDTG9_5zUwWq3DTxsiiEUYHsphS2EJLRrq4k-5d2ghOAgSBMgbPHAbntyNrshCdVv70pmM1_3nQ-O_lJO3_xKXGmtxiQy_28iGfl6YMFFylEv11fzxXbZIdvrt_oqGGIyYymxBAg_tZBQ93QfFsENm000F__0m00)

6. Hệ thống con: Quản lý Báo cáo
Mô tả: Chức năng chính: Tạo và quản lý các báo cáo tài chính và nhân sự của hệ thống.

Thành phần chính:

Tạo Báo cáo Lương:
Tổng hợp dữ liệu về lương của tất cả nhân viên, bao gồm lương cơ bản, phụ cấp, khấu trừ, và tổng lương.
Cho phép tạo báo cáo theo thời gian (theo ngày, tuần, tháng, năm) hoặc theo bộ phận.
Báo cáo Thời gian làm việc:
Tổng hợp và báo cáo số giờ làm việc của nhân viên trong một khoảng thời gian cụ thể.
Cho phép xuất báo cáo theo bộ phận hoặc cá nhân.
Báo cáo Tình trạng Người dùng:
Cung cấp báo cáo về tình trạng tài khoản người dùng (có thể bao gồm số lượng người dùng đăng nhập trong ngày, số lượng tài khoản bị khóa, v.v.).
Báo cáo về các quyền truy cập của người dùng và sự thay đổi quyền hạn.
Quản lý Xuất Báo cáo:
Xuất báo cáo dưới các định dạng phổ biến như PDF, Excel hoặc CSV.
Tự động gửi báo cáo qua email đến các quản lý hoặc bộ phận liên quan.
![subsystem diagram](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3bT1Od9sOdggWb9WwSDTY_CKSWxlLN0wl31V8Hb8A2bKSoae9ESa5XShA4KytBqMBEtoSFTwXPpCXxlRIz6LAYZeAeGyt3qrBrqXu-7knGKAAGYrK6cuCQXIjGYBGXxk0XgArMIGH19CGk78n8Uxk_Co5B8VxjwCGqb9Hcg-GkNXLQKAoGztBOTOLClba9gN0l8y0000__y30000)
