1. Create Administrative Report
1.1. Xác định các lớp phân tích:
Payroll Administrator (Quản trị viên tiền lương): Thực hiện yêu cầu tạo báo cáo.

Payroll System (Hệ thống trả lương): Quản lý và tạo báo cáo dựa trên thông tin yêu cầu.

Report (Báo cáo): Đại diện cho báo cáo được tạo ra.

1.2. Mô tả hành vi qua biểu đồ Sequence:
https://www.planttext.com/api/plantuml/png/Z9AnJiCm48RtFCKf4qZb1JgWAbawTAba8HXJWnABu4JfkH8Z4mDJtu1G8QHA5SpEqC6ex-4du1KukofA8uXOBCl-_hl_VlkhsOxcc5Iexl8WuLXK44wLrIi9MDdc2HR2h2KmOPi72VdkOrVBD8Ha3bDsmIP1ILB1HPb8X71icqV0p3PBcGAhgCgHOiowWiZK1N1Q_7qK1u6l2cVd7Xx2bLahu5Q_AK2h2PuT58437EWLnwJm-yniMdYdSAp88k6lvQyudEG5zHC3aAbvleUPrUy8dqjN_t1sQ_KMQLoZ-G3GfIGpyoBtYPt--8lY8R1-xoqpVnfkpKUPgdy5iN0FY1KDvYGz4NJ0jlL9RxDBKtCQs-gDf7JCgkjjT2EltS_w1W00__y30000

1.3. Nhiệm vụ của từng lớp phân tích:
Payroll Administrator: Đưa ra yêu cầu và tiêu chí tạo báo cáo.

Payroll System: Nhận yêu cầu, tạo và lưu báo cáo.

Report: Lưu trữ thông tin báo cáo.

1.4. Thuộc tính và quan hệ giữa các lớp:
Payroll Administrator: Có thuộc tính như adminId, name.

Payroll System: Liên kết với Report và Payroll Administrator, điều phối việc tạo báo cáo.

Report: Bao gồm thuộc tính như reportType, startDate, endDate.
2. Create Employee Report
2.1. Xác định các lớp phân tích:
Employee (Nhân viên): Thực hiện yêu cầu tạo báo cáo.

Payroll System (Hệ thống trả lương): Tạo báo cáo dựa trên thông tin yêu cầu.

Report (Báo cáo): Đại diện cho báo cáo được tạo ra.

Project Management Database (Cơ sở dữ liệu quản lý dự án): Cung cấp thông tin về dự án cho báo cáo.

2.2. Mô tả hành vi qua biểu đồ Sequence:

https://www.planttext.com/api/plantuml/png/b5EnIiDG5Dtp5OTC2le37KIR3Xs2KCoWO_egQJ1zAUbBeL_W80uT71p4nY92eLJNFAJ3a_x7-m9_mPj89AcLrWmXt7lEFVUUU_CfbyS3uKOYxWM6oqGOmJpjgYUEeQzct3JwbFEPttUvWDdKyXgYg-MOUt0YdKuHh5vN2VTCk0Cq7SUk4keg2S7ebUVhLZLhhH8Cj7n4Gyi50f-gnsZ5L9OZKEzP-0qguJdPEclOBRjnOXYL1d5ubElMSA5cCPXENs88dP9kkn0tCa06h32h33__xgfvYVQ7a1NJz4Hxxc-aOIy8ITy_0FVKP8IsJXS27-DCfuXTwNGfo4cLidt33GJid58g4gW9J4VBEz8YZyRmo9w7BDoZXiWfHh8XUbhU2tGAempGKqnRE5Q3JSsEliiKq1nP83REzXk-tKP6jt7BDr2tMrdbNFBEpzRgLWtERXijrTkwnbBRTCJnlyvbgEKDH4HhpwWx7CeQeJoQlPFukKeOU5UdSqwtfARhFH-JOza__0K00F__0m00

2.3. Nhiệm vụ của từng lớp phân tích:
Employee: Đưa ra yêu cầu và tiêu chí tạo báo cáo.

Payroll System: Nhận yêu cầu, tạo và lưu báo cáo.

Report: Lưu trữ thông tin báo cáo.

Project Management Database: Cung cấp thông tin về dự án.

2.4. Thuộc tính và quan hệ giữa các lớp:
Employee: Có thuộc tính như employeeId, name.

Payroll System: Liên kết với Report, Employee, và Project Management Database, điều phối việc tạo báo cáo.

Report: Bao gồm thuộc tính như reportType, startDate, endDate.

Project Management Database: Lưu trữ thông tin dự án.

3. Login
3.1. Xác định các lớp phân tích:
User (Người dùng): Người dùng đăng nhập vào hệ thống.
Payroll System (Hệ thống trả lương): Xác thực thông tin đăng nhập.

3.2. Mô tả hành vi qua biểu đồ Sequence:
https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3bTYSab-aOAIN_gn3GztpyrKI3cyCozTYQi0A9sPd5cGc5UYeEJnS7UxGad6mzqJyz8LGeeUxbgia7Dimx65G8KAYSKA7Y4XFbnSw4OewDg1PQmK_38UxbfRe51oU5MUGjdX1GgvG6w9GZPGT6Kf5qW9Gcd4uON9O9isWgZ3Mu3sbMJcSINcb2Y4mBaAGFd51GevG5TnAG01p0Xq5rWf79bmf1ce9m_gW8p32_8o5991vd2bvXId8fkP3M4IRRH7viFTpNbWjtR3d9fqU64-IE_qJAxKl1Gk1o012c800000__y30000

3.3. Nhiệm vụ của từng lớp phân tích:
User: Nhập thông tin đăng nhập.

Payroll System: Xác thực thông tin đăng nhập và phản hồi kết quả.

3.4. Thuộc tính và quan hệ giữa các lớp:
User: Có thuộc tính như username, password.

Payroll System: Xác thực thông tin đăng nhập của User.

4. Maintain Employee Information
4.1. Xác định các lớp phân tích:
Payroll Administrator (Quản trị viên tiền lương): Thực hiện các thay đổi thông tin nhân viên.

Payroll System (Hệ thống trả lương): Quản lý và lưu trữ thông tin nhân viên.

Employee (Nhân viên): Đại diện cho thông tin nhân viên.

4.2. Mô tả hành vi qua biểu đồ Sequence:
https://www.planttext.com/api/plantuml/png/v5I_IiD06D_lAJuwATGNw225BXbAe72KEXvfQGB99IGNiQCuE7GgFa4i8WG5GQTaS3ZfUzmJ-0hzxbHiMbCRLpCao_Vx-ttalNpj9eB58WrymXmHnj0QfAfOSX2nAkTmxicS0_LKUSd1NpsjCZvj0KjWG8UqJoA4UeuNCIwWPQdo6eIhoWMV0esHfOAmw3R0TkKj_v0m4_QG4CCB9wTcl0DdCa_1KSLz2kDqXgRa0qh85rGG7WV-pK0qG0CDGmNfXwh8FCIn48JC73YYhio3DlHKyHWX2Nv46qRocHrl6-YbA8KqTz4E3M6-0CDKyG7ur7kfCQz1zSfxG5zAzh035Fs5W0kuWMIL_MPgf9imsJcyBUHIgsn5cVZ9f59IWw01CXwUyAVfpMXzd9eTqiEd4GilzegRQvmtw7op4sSpzu4Rw3N4rAt2gUlSR4GVwd_QnCM-lDgJAUJFTxz3F-5ZqiMN_Yck0G00__y30000

4.3. Nhiệm vụ của từng lớp phân tích:
Payroll Administrator: Thực hiện các thao tác thêm, cập nhật, và xóa thông tin nhân viên.

Payroll System: Xử lý và lưu trữ thông tin nhân viên.

Employee: Lưu trữ thông tin chi tiết về nhân viên.

4.4. Thuộc tính và quan hệ giữa các lớp:
Payroll Administrator: Có thuộc tính như adminId, name.

Payroll System: Liên kết với Employee và Payroll Administrator, điều phối việc quản lý thông tin nhân viên.

Employee: Bao gồm thuộc tính như employeeId, name, address, salary.
5. Maintain Purchase Order
5.1. Xác định các lớp phân tích:
Commissioned Employee (Nhân viên hoa hồng): Thực hiện các thay đổi thông tin đơn hàng.

Payroll System (Hệ thống trả lương): Quản lý và lưu trữ thông tin đơn hàng.

Purchase Order (Đơn hàng): Đại diện cho đơn hàng.

5.2. Mô tả hành vi qua biểu đồ Sequence:
https://www.planttext.com/api/plantuml/png/t9InIiDG68Nt-nI7JWhr1Jf8eKk6qYb87IzfQGBfJKXlnCuE3Yujle2rY50K19sImU6MliTz0b_1_wQjD5vR8cvcI20vv_p_-RZa8tzlZYHFP3eC6VTabA3MyTMzm4MW5W9EnE7h_5OCQk0ZTCwS5ej97dX1p8L4pT7vDIH9fc80Dz7P7E7gPJNR61pNRPSDombzXA_kDehbn67CvEBaj90tSAuMAJoTFQRefMF8H3rXEVsoCQCoQkCggSD8PxE0rk4Hf9fvE7BfHLH7IsVFCOHF3rb7LxtousypModjJoaFiPN2U2XH19Ms05rxDv6-UgD06GZBitVk0Szs3i5gL5gbQzeNVKsOcaDQfduuwfV0L6ytfC3AjNuIRvFNuZRfnbNghnTn0frVYUBGtVmLjBVJtoRz2peMS6-Vj-1kZk3_vhqBvF9Gsu9q1HuMOIkrBtgiIJVpB_i4003__mC0

5.3. Nhiệm vụ của từng lớp phân tích:
Commissioned Employee: Thực hiện các thao tác thêm, cập nhật và xóa thông tin đơn hàng.

Payroll System: Xử lý và lưu trữ thông tin đơn hàng.

Purchase Order: Lưu trữ thông tin chi tiết về đơn hàng.

5.4. Thuộc tính và quan hệ giữa các lớp:
Commissioned Employee: Có thuộc tính như employeeId, name.

Payroll System: Liên kết với Purchase Order và Commissioned Employee, điều phối việc quản lý thông tin đơn hàng.

Purchase Order: Bao gồm thuộc tính như orderId, customerContact, billingAddress, productDetails, date.

6. Run Payroll
6.1. Xác định các lớp phân tích:
Payroll System (Hệ thống trả lương): Quản lý và tính toán bảng lương.

Employee (Nhân viên): Nhận lương từ hệ thống.

Bank System (Hệ thống ngân hàng): Thực hiện chuyển khoản cho nhân viên.

6.2. Mô tả hành vi qua biểu đồ Sequence:
https://www.planttext.com/api/plantuml/png/X98nQiCm58Ptd-AHlHV8K48d5uBfO49NLmcMgFCSOhcGiNJeq2atY1jAII4qGo4W3HbKSeztWbwXJqcmuwNLO67y_x--_ra_TjShT3BLvJWB9hmheIO9QkY4P9z1Ix9pJ26Uabb2jj_iAqmxa1GGnd6_ROYaUqLuKEu33ufey4TWb7gnT8iwBWg3m8V2nUKXl0jNP3urVC_9l9SW99bg1dVCmVOJIMs81bteatcRyG7kYmLQ8M0318934FHvZPOvTckKe7DNOVqzoJJSoEFB0NmbU4iQdLimLZaZ-uHmBtEF5W2lfaOKSZI3vv2g98SXsHSX0Plo9tqKDhLlNIMOdSmQMoxj3HA4xnUCicBqBvnMP1yHncIs6ZpVLa3XLg85wTjV8qoa8hChw_8Z7BO6T4vrql2lSKj-x3Tab-8utA37Hd-NVW400F__0m00

6.3. Nhiệm vụ của từng lớp phân tích:
Payroll System: Quản lý quy trình tính toán và thanh toán lương.

Employee: Nhận lương từ hệ thống.

Bank System: Thực hiện chuyển khoản cho nhân viên.

6.4. Thuộc tính và quan hệ giữa các lớp:
Payroll System: Liên kết với Employee và Bank System, điều phối việc tính toán và thanh toán lương.

Employee: Có thuộc tính như employeeId, name, paymentMethod.

Bank System: Liên kết với Payroll System để thực hiện chuyển khoản.

