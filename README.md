# 1. Create Administrative Report

## 1.1. Xác định các lớp phân tích:
- **Payroll Administrator (Quản trị viên tiền lương)**: Thực hiện yêu cầu tạo báo cáo.
- **Payroll System (Hệ thống trả lương)**: Quản lý và tạo báo cáo dựa trên thông tin yêu cầu.
- **Report (Báo cáo)**: Đại diện cho báo cáo được tạo ra.

## 1.2. Mô tả hành vi qua biểu đồ Sequence:
![Sequence Diagram](https://www.planttext.com/api/plantuml/png/Z9AnJiCm48RtFCKf4qZb1JgWAbawTAba8HXJWnABu4JfkH8Z4mDJtu1G8QHA5SpEqC6ex-4du1KukofA8uXOBCl-_hl_VlkhsOxcc5Iexl8WuLXK44wLrIi9MDdc2HR2h2KmOPi72VdkOrVBD8Ha3bDsmIP1ILB1HPb8X71icqV0p3PBcGAhgCgHOiowWiZK1N1Q_7qK1u6l2cVd7Xx2bLahu5Q_AK2h2PuT58437EWLnwJm-yniMdYdSAp88k6lvQyudEG5zHC3aAbvleUPrUy8dqjN_t1sQ_KMQLoZ-G3GfIGpyoBtYPt--8lY8R1-xoqpVnfkpKUPgdy5iN0FY1KDvYGz4NJ0jlL9RxDBKtCQs-gDf7JCgkjjT2EltS_w1W00__y30000)

## 1.3. Nhiệm vụ của từng lớp phân tích:
- **Payroll Administrator**: Đưa ra yêu cầu và tiêu chí tạo báo cáo.
- **Payroll System**: Nhận yêu cầu, tạo và lưu báo cáo.
- **Report**: Lưu trữ thông tin báo cáo.

## 1.4. Thuộc tính và quan hệ giữa các lớp:
- **Payroll Administrator**: Có thuộc tính như `adminId`, `name`.
- **Payroll System**: Liên kết với `Report` và `Payroll Administrator`, điều phối việc tạo báo cáo.
- **Report**: Bao gồm thuộc tính như `reportType`, `startDate`, `endDate`.

---

# 2. Create Employee Report

## 2.1. Xác định các lớp phân tích:
- **Employee (Nhân viên)**: Thực hiện yêu cầu tạo báo cáo.
- **Payroll System (Hệ thống trả lương)**: Tạo báo cáo dựa trên thông tin yêu cầu.
- **Report (Báo cáo)**: Đại diện cho báo cáo được tạo ra.
- **Project Management Database (Cơ sở dữ liệu quản lý dự án)**: Cung cấp thông tin về dự án cho báo cáo.

## 2.2. Mô tả hành vi qua biểu đồ Sequence:
![Sequence Diagram](https://www.planttext.com/api/plantuml/png/b5EnIiDG5Dtp5OTC2le37KIR3Xs2KCoWO_egQJ1zAUbBeL_W80uT71p4nY92eLJNFAJ3a_x7-m9_mPj89AcLrWmXt7lEFVUUU_CfbyS3uKOYxWM6oqGOmJpjgYUEeQzct3JwbFEPttUvWDdKyXgYg-MOUt0YdKuHh5vN2VTCk0Cq7SUk4keg2S7ebUVhLZLhhH8Cj7n4Gyi50f-gnsZ5L9OZKEzP-0qguJdPEclOBRjnOXYL1d5ubElMSA5cCPXENs88dP9kkn0tCa06h32h33__xgfvYVQ7a1NJz4Hxxc-aOIy8ITy_0FVKP8IsJXS27-DCfuXTwNGfo4cLidt33GJid58g4gW9J4VBEz8YZyRmo9w7BDoZXiWfHh8XUbhU2tGAempGKqnRE5Q3JSsEliiKq1nP83REzXk-tKP6jt7BDr2tMrdbNFBEpzRgLWtERXijrTkwnbBRTCJnlyvbgEKDH4HhpwWx7CeQeJoQlPFukKeOU5UdSqwtfARhFH-JOza__0K00F__0m00)

## 2.3. Nhiệm vụ của từng lớp phân tích:
- **Employee**: Đưa ra yêu cầu và tiêu chí tạo báo cáo.
- **Payroll System**: Nhận yêu cầu, tạo và lưu báo cáo.
- **Report**: Lưu trữ thông tin báo cáo.
- **Project Management Database**: Cung cấp thông tin về dự án.

## 2.4. Thuộc tính và quan hệ giữa các lớp:
- **Employee**: Có thuộc tính như `employeeId`, `name`.
- **Payroll System**: Liên kết với `Report`, `Employee`, và `Project Management Database`, điều phối việc tạo báo cáo.
- **Report**: Bao gồm thuộc tính như `reportType`, `startDate`, `endDate`.
- **Project Management Database**: Lưu trữ thông tin dự án.

---

# 3. Login

## 3.1. Xác định các lớp phân tích:
- **User (Người dùng)**: Người dùng đăng nhập vào hệ thống.
- **Payroll System (Hệ thống trả lương)**: Xác thực thông tin đăng nhập.

## 3.2. Mô tả hành vi qua biểu đồ Sequence:
![Sequence Diagram](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3bTYSab-aOAIN_gn3GztpyrKI3cyCozTYQi0A9sPd5cGc5UYeEJnS7UxGad6mzqJyz8LGeeUxbgia7Dimx65G8KAYSKA7Y4XFbnSw4OewDg1PQmK_38UxbfRe51oU5MUGjdX1GgvG6w9GZPGT6Kf5qW9Gcd4uON9O9isWgZ3Mu3sbMJcSINcb2Y4mBaAGFd51GevG5TnAG01p0Xq5rWf79bmf1ce9m_gW8p32_8o5991vd2bvXId8fkP3M4IRRH7viFTpNbWjtR3d9fqU64-IE_qJAxKl1Gk1o012c800000__y30000)

## 3.3. Nhiệm vụ của từng lớp phân tích:
- **User**: Nhập thông tin đăng nhập.
- **Payroll System**: Xác thực thông tin đăng nhập và phản hồi kết quả.

## 3.4. Thuộc tính và quan hệ giữa các lớp:
- **User**: Có thuộc tính như `username`, `password`.
- **Payroll System**: Xác thực thông tin đăng nhập của `User`.

---

# 4. Maintain Employee Information

## 4.1. Xác định các lớp phân tích:
- **Payroll Administrator (Quản trị viên tiền lương)**: Thực hiện các thay đổi thông tin nhân viên.
- **Payroll System (Hệ thống trả lương)**: Quản lý và lưu trữ thông tin nhân viên.
- **Employee (Nhân viên)**: Đại diện cho thông tin nhân viên.

## 4.2. Mô tả hành vi qua biểu đồ Sequence:
![Sequence Diagram](https://www.planttext.com/api/plantuml/png/v5I_IiD06D_lAJuwATGNw225BXbAe72KEXvfQGB99IGNiQCuE7GgFa4i8WG5GQTaS3ZfUzmJ-0hzxbHiMbCRLpCao_Vx-ttalNpj9eB58WrymXmHnj0QfAfOSX2nAkTmxicS0_LKUSd1NpsjCZvj0KjWG8UqJoA4UeuNCIwWPQdo6eIhoWMV0esHfOAmw3R0TkKj_v0m4_QG4CCB9wTcl0DdCa_1KSLz2kDqXgRa0qh85rGG7WV-pK0qG0CDGmNfXwh8FCIn48JC73YYhio3DlHKyHWX2Nv46qRocHrl6-YbA8KqTz4E3M6-0CDKyGAm-J8NMRw5A==)

## 4.3. Nhiệm vụ của từng lớp phân tích:
- **Payroll Administrator**: Chỉnh sửa thông tin nhân viên.
- **Payroll System**: Lưu trữ và cập nhật thông tin nhân viên.
- **Employee**: Đại diện cho thông tin nhân viên.

## 4.4. Thuộc tính và quan hệ giữa các lớp:
- **Payroll Administrator**: Có thuộc tính như `adminId`, `name`.
- **Payroll System**: Quản lý thông tin của `Employee`.
- **Employee**: Đại diện cho các thuộc tính như `employeeId`, `name`.

---

# 5. Generate Payroll Report

## 5.1. Xác định các lớp phân tích:
- **Payroll Administrator (Quản trị viên tiền lương)**: Yêu cầu tạo báo cáo tiền lương.
- **Payroll System (Hệ thống trả lương)**: Xử lý và tạo báo cáo tiền lương.
- **Report (Báo cáo)**: Đại diện cho báo cáo tiền lương.

## 5.2. Mô tả hành vi qua biểu đồ Sequence:
![Sequence Diagram](https://www.planttext.com/api/plantuml/png/hVNdYy8i5Q15gm8rtHhYPWLSm1A7Qb56wn6woicOprKEm6bTbq3t-MsSEkNUDq5UMXbHfKYHkxiHrCpzxf-12Rz_6MfGHltcAhNEuNw0fR40ctLGg6wotnSIZp29eITXZzntzFqlMj_Gb4OTe5-Vf_jtAq4cb91zOtEowzsm5ga-VNRav5jxya_1gB34kjBqjiEzeIkwtVVsaMPbg7kFBz7I0Whh9b48PvD5w-7UNdeA0F_k8PQ9ETqKlHqg9qxZzXgH54cNY5Aqg0g7RzoM9oFCXvk=)

## 5.3. Nhiệm vụ của từng lớp phân tích:
- **Payroll Administrator**: Đưa ra yêu cầu và tiêu chí tạo báo cáo tiền lương.
- **Payroll System**: Tạo báo cáo tiền lương.
- **Report**: Lưu trữ báo cáo tiền lương.

## 5.4. Thuộc tính và quan hệ giữa các lớp:
- **Payroll Administrator**: Có thuộc tính như `adminId`, `name`.
- **Payroll System**: Quản lý thông tin báo cáo tiền lương.
- **Report**: Bao gồm các thuộc tính như `salary`, `bonus`, `deductions`.
# 6. Generate Payment Report

## 6.1. Xác định các lớp phân tích:
- **Payroll Administrator (Quản trị viên tiền lương)**: Yêu cầu tạo báo cáo thanh toán.
- **Payroll System (Hệ thống trả lương)**: Xử lý và tạo báo cáo thanh toán.
- **Report (Báo cáo)**: Đại diện cho báo cáo thanh toán.

## 6.2. Mô tả hành vi qua biểu đồ Sequence:
![Sequence Diagram](https://www.planttext.com/api/plantuml/png/xVBDI8m43B95fL5ay88H8RNN70b8V2gMjp3mvqexOzh2yNCtTSxy5KnobVfhh1boh-4MEC9yD_JA3Kxks-T2YMBFgLv8QsK9j2M2UNuLpfqZ0he8uNjsNDRjeUJfVNB2A7gtqD0S_mWsJ9h7d1HV2p8oHpxyhv9cI-wrWks3CkVJlODVRRkDNf_Qpegl1Cya_Mx6UJ4esH0zKHwa-WfhkOs_AwDbAs2rrbW02lcdbuROr7scdV2u6p9SovPq9r3V1nE7X5ztswmr57UJc4Dmt_gNKYevXUMzPU5_AmiZlAfpBej__f1f-l1hhzQkA==)

## 6.3. Nhiệm vụ của từng lớp phân tích:
- **Payroll Administrator**: Đưa ra yêu cầu và tiêu chí tạo báo cáo thanh toán.
- **Payroll System**: Tạo báo cáo thanh toán dựa trên yêu cầu của quản trị viên.
- **Report**: Lưu trữ thông tin báo cáo thanh toán.

## 6.4. Thuộc tính và quan hệ giữa các lớp:
- **Payroll Administrator**: Có thuộc tính như `adminId`, `name`.
- **Payroll System**: Quản lý việc tạo báo cáo thanh toán.
- **Report**: Bao gồm các thuộc tính như `paymentAmount`, `paymentDate`, `paymentMethod`.
