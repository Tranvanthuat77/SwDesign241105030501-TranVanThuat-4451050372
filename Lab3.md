# Lab 3. Identify Design Elements

# Xác định các phần tử thiết kế của hệ thống “Payroll System”

## 1. Subsystem Context Diagrams

#### Biểu Đồ Ngữ Cảnh Hệ Thống Con BankSystem

![Context Diagram for BankSystem Subsystem](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3bTcNabgKLfYSgg2frDYNdPmPN59Qgv2DPS22AG_tBqsCoJpuUx6F8tYXxidGfXM2YdvfKavgJeAOB732pAzC_8VxbeCb0WkAShCIzVagkNYIiv9B2vMy7Yukpqa0wWiBzql_V2YF8_32_BI5J9p2t9ISrFpIeffOsj0HkR3NVjBVOvjEBOGQ1tKN4op8E9vwOSNL5efk2IMf28fnBG0ONv8nk4jUUaXcNb8Ve9QKd9u5P8eN2iXSuzC03cir1leyDtDUI55G7cOwtLrxP13YGivn6ngT7MnXp4Nzf3F1wf73Hqy2h5uayiXDIy5b6u00000__y30000)

**Giải thích:**

- **ĐiềuKhiểnTrảLương**: Thành phần điều khiển quy trình trả lương.
- **IBankSystem**: Giao diện định nghĩa phương thức gửiTiền để gửi tiền vào ngân hàng.
- **HệThốngNgânHàng**: Hệ thống con triển khai phương thức gửiTiền.
- **PhiếuLương**: Thực thể đại diện cho phiếu lương.
- **ThôngTinNgânHàng**: Thực thể đại diện cho thông tin ngân hàng.

Biểu đồ này cho thấy ĐiềuKhiểnTrảLương có thể thực hiện quy trình trả lương và trực tiếp gửi tiền vào ngân hàng thông qua giao diện IBankSystem, giao diện này được triển khai bởi hệ thống con HệThốngNgânHàng.

#### Biểu Đồ Ngữ Cảnh Hệ Thống Con PrintService

![Biểu Đồ Ngữ Cảnh Hệ Thống Con PrintService](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3bTcNabgKLfYSgg2fyl3tTt96M4FTo_rp7kuQqcUGZMN0WXavcaKP6G-tBM_rEVOXcCByzAj509G-9fSjLnSoJc9nSKA66PavXRafEQcvfKKKyS2L0cO2SKFTqyCoNoukp7FIY4blpGf9nKYdfT-U46bbO9BOaagmeYGZCDRyj93ClDGNL5oU5MUx-65bPv0Cu9BYZBpqX5cEptSjJWF904CBf11HoQ0B2lr1ZfcTtDUI15G6kOYNLqxJ9zoOVhTfaPN5oEuk32KvGDLeVePkneqJt4vfEQbWE8N0000__y30000)

**Giải thích:**

- **ĐiềuKhiểnTrảLương**: Thành phần điều khiển quy trình trả lương.
- **IDịchVụInẤn**: Giao diện định nghĩa phương thức in để in phiếu lương.
- **DịchVụInẤn**: Hệ thống con triển khai phương thức in.
- **PhiếuLương**: Thực thể đại diện cho phiếu lương.
- **ThôngTinInẤn**: Thực thể đại diện cho thông tin in ấn.

Biểu đồ này cho thấy ĐiềuKhiểnTrảLương có thể yêu cầu in phiếu lương thông qua giao diện IDịchVụInẤn, giao diện này được triển khai bởi hệ thống con DịchVụInẤn.

#### Biểu Đồ Ngữ Cảnh Hệ Thống Con ProjectManagementDatabase

![Biểu Đồ Ngữ Cảnh Hệ Thống Con ProjectManagementDatabase](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3bTcNabgKLfYSgg2ftEmYqzWwSDTY_Dy3kzrURXxu-76F8LgBWKGo7cuQscbSqPcIER3NVjBe98QkOSNGvbM2i4bHPbvwPf8og5IVXc75-M5PHvU1LQFu26qr79n9USa5XShO7L1Pcv1JcfkQbv9yQ1m8fe5CDinxO68bm2DmIgHbtvuGQNJmrthIuvCUBXhUQcLWajYIIgId3V8bf2CmxkIeL9mDs2u6iaHc8x7wJwWUKScP3xStLZgdG6aclD2Ye0XwtDimx65UUaAkhfssCER2tiisDJewcADG2wiolD1gj724hTA31zpEQJcfO3IBm000F__0m00)

**Giải thích:**

- **ĐiềuKhiểnTrảLương**: Thành phần điều khiển quy trình trả lương và các tác vụ liên quan đến dự án.
- **ICSDLQuảnLýDựÁn**: Giao diện định nghĩa các phương thức để lấy thông tin về dự án và các dự án của nhân viên.
- **CSDLQuảnLýDựÁn**: Hệ thống con triển khai các phương thức của giao diện ICSDLQuảnLýDựÁn.
- **ChiTiếtDựÁn**: Thực thể đại diện cho chi tiết dự án.
- **DựÁnNhânViên**: Thực thể đại diện cho các dự án mà nhân viên tham gia.

Biểu đồ này cho thấy ĐiềuKhiểnTrảLương có thể tương tác với cơ sở dữ liệu quản lý dự án thông qua giao diện ICSDLQuảnLýDựÁn. Giao diện này được triển khai bởi hệ thống con CSDLQuảnLýDựÁn, hệ thống này quản lý chi tiết dự án và các dự án của nhân viên.

---

## 2. Ánh xạ các lớp phân tích đến các phần tử thiết kế

### Create Administrative Report

![Mapping Analysis Classes to Design Elements - Create Administrative Report](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3bToJc9niOAIqyDTY_FI5GutvcKeH3pSjL31kIWriIHLmJ4bDpClixYaAB4aionL8IYr8B-eH4aXiLZ1Dx6W83ClFIGnAIVLKA6QIm48QXHy7kwUNQ0Ga75uKPv2oE6roHaAoA06AFDmrtAWrCFTQnL2CZ8VxjfVek0D915A80RfuWPuvA2Q5G8IAuloStAGNPzV17K1M0pY3xVyebm5T9lXceChYqjIaUH1SX1zxgbvgGWZKJH352XW0J0vb_paqjpKF6GrDLorN0wfUIcW-000003__mC0)

### Create Employee Report

![Mapping Analysis Classes to Design Elements - Create Employee Report](https://www.planttext.com/api/plantuml/png/V94zJWCn48NxFSKeFGqdY2204215i0Njn0oxGVwJFIbMR8gS8rMWeCe5TeiKUnAVW2jWM287hSWhNCpdDs_6_cntOy_eUA5a9YHw3wEpqBph0hgLBk4nD1iuTuHCSA6iD1KHt9CrZaU07kxGshakSfn9EeNN3A9gk0tjsiAqxDuqvDrMb72eEfBGV4GKsYtavJmqEuQRUAOhVQEJ_tM4_PhJl0CbrgzoQPpwcmnJh9oH4XugpwIEcQz8aqCsBfbxCCmTcYT6B1HfFansveK4nwVLMD0Fd23Z33qbkgzSQoRtZ8BgR9cDIJzz_-CN0000__y30000)

### Login

![Mapping Analysis Classes to Design Elements - Login](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3bToJc9niOAIqyDTY_FI5GutvcKeH3pSjL319pyzCqz98R5OmJUne20pBpqaCIadrLYXcai126eKV1xkdbsW491nU56UGiZXjSaP2iYW1YZpSDToeDJ3tMiLGZ8o7-xQNwBW3IGHIY06wU86UEIWcXL2YrEB5B226eWFtFABSZ6ae9e34YkBydDo588hYqjISr4rEvQMPAJcbMGc9vPavkS5fnQLPIQdGZJNSZcavgM0mWu0003__mC0)

 ### Maintain Employee Information

![Mapping Analysis Classes to Design Elements - Maintain Employee Information](https://www.planttext.com/api/plantuml/png/V94zJWCn48NxFSLJUZeE47ub194YPGlQ8J6xbkpnofuKAqB1EQY0WYeNs2rIx4by0gw0LoJPH0YUP3VVUvuVVxMRSH3oihGccniA0QFps7nmWUw5Izp7vWqJqYpfuCfMnjLAuOOVdRSasl4859AZgZGNEJqOTOgd34ahtCNsjSAqxDuPURUUbpZKAf7OV2OKspNoKiTc8xXDzs3vUUZaR_t3jc5CgVRE69mjh6OTn9Cul-rWDz24c0fb5Sjrcckel0_FwY3A7hU_2r-Iq8LZwOtA7uJtw_gbWVMRF4RPSpPMlEW_v1i00F__0m00)

### Maintain Purchase Order

![Mapping Analysis Classes to Design Elements - Maintain Purchase Order](https://www.planttext.com/api/plantuml/png/V54xJWCn4Ett54_fAUaZ8f0GHAp45hHcTuWjsUELxHGhGi4vg4WAgbnWjqYn9_49k08E9Cec4ddIJFFcpPlFTxSP-o1Sc1kTbLfuZz5LR5SyG__E4a-n_SHKA0ufaCzTAOKdFBYAt0Z29wwk5SyAyQpf4gyP4XQuZzr7ZLpsIqRHhqk98HQ9YUrNecAtHY5LR3S1ToaVIluQNVoFCznEZ8arHdclB5E5QrDhsn3j9zYjyhl9ZNNcn1cvQ9pL6e-D3sHEnX-A9vR3jfBSG7nqg3FYMtwn1-UtR4nSRL_n0m00__y30000)

### Run Payroll

![Mapping Analysis Classes to Design Elements - Run Payroll](https://www.planttext.com/api/plantuml/png/V90zRi9048Lxd-A9dZOrGaf58bdW8kra6M6BzQorkqIo0WNde28fKd41kw3mIVO4N04J207oyufflddpdcPNRtlEa_MpN4TAatFez4FrBXCqIqdn5AerXZD1JAKrMdT03ezK59bC4dhMV8VN2AtcU0Zrga2SDc-2fDce59UQjoHK7oqAzGP9ceLgwp5ev_VAyL3tR_t3JkQldXYLpdD-q-38OciKEsViRJBkyqARaXa_T3OFMHaxla8dSvza-alicIMMn97ocP4HsvTCyQTv4VLOneVtxm400F__0m00)

### Select Payment

![Mapping Analysis Classes to Design Elements - Select Payment](https://www.planttext.com/api/plantuml/png/V9AnJiCm48RtFCMfEpDhLOakK14f6LXTzwWZxBDb6wI8CF0SJBG3KryW6JhaIVm4l0AEsg3IfFo3b__qtV_h_Dtifyupwv-LJBXapi5a5kejhQ5z9m4FeVw432Lo3oah5PAV07EmOCOKjCxPKk8rl2OGLS5TQ3uCfABT4EJjZWiuLHMTK7z5ApGxo4KHwhs7s_Z-7Jl0hYxhFw-pZsbkb96wH8I1ghxBeLcXQQwjEa_G3Laj9MIbywX60QdL79tJTgn2FmGBz4AlHW7tfbi_27W4p1WzZQp_zNBBo3sYpT2-51o7W3x1CETvXNZDKqgLl2LJf5NtBtu0003__mC0)

### Maintain Timecard

![Mapping Analysis Classes to Design Elements - Maintain Timecard](https://www.planttext.com/api/plantuml/png/V94zQiD044PxdM9mdpwbCN6Q921i5Mx7wy7Qi3zYTXCGLWgVmrMI8fKl81KkT98zGQwG5N6CZHH_i5li-tZCiD_DOUmyid_HAX4AdOFH9DIVPWtjrkIm2FKxFA4qFXx8f2Q1l1e1klXQ5DAiCrmgkeLD0Z4LF8PcLq2Qjn-ntkv53kUf8WdrLqIXsKEMor0VF3p4-xBsAxlvFzTOXu_JJ7MXR4a4lLIdPQR6StblMGzCS2fT4yn8s5xZJv1YoLOfc9VEanuMf6m5EMTvKC3scOI7E_IuH4VdWYFhq9puLGgw4BmbOpAhxcT_0000__y30000)

---

## 3. Ánh xạ các phần tử thiết kế vào các gói

![Mapping Design Elements to Packages](https://www.planttext.com/api/plantuml/png/d9CxRi9048PxJZ6Yj9GBkE8HG2X1GiAHqcxM4pnY7sXt0LaXHOuIfOXIf4fd2WfEuXFa2h5vH2QnaU0ljjZvzvj_f9tlrRfX7JDk9aMD2sOjr5jfygR6i7bH4TodoIiCepHvLn2agqy88agJjOERxAm3it2DbiQg8r2YSW5x40XFDSYq1C-hUkbvi5Dkwcs-2DfHklfWl_TbMkwmLoTqidXat4UyrMDINMraIJiOK1WAN323lZz2FZFaOj_ltVMXQvZ4XJQJGYuOC58TEHKwHlo3N49pEXN4cIEjhEyVRD3aZkRa2EtHZ12GHCvCM1BjR5QUg_2aY3nxnaEkjbREQ27GN9vh55k7iYqqd_ILG_F8E5QmXYpEkrN-2TWRIc9TnE8Hyib_HrPipImfpDPaX6PE70l0fd6KpU3iblLSQw0AyxNw0G00__y30000)

---

## 4. Các lớp kiến trúc và mối quan hệ giữa chúng

![Architectural Layers and Their Dependencies](https://www.planttext.com/api/plantuml/png/T95D3e8m48NtFKNZdYiO8BfpOMHfM8nrGYQKqhI5X1XFvi8ZUGL5KChVzdlJzzvCNuzdQ1qOLnMIQH0vPCWtaTQI13WgbUK7QD1i-8rnVjuNMfODOYGSrUG8RSfRVeJ6b59wkAK9YigGQr9sPuDvN5bIQ2rFqDGaS9pGE_NQroO6bPFAV7H2NHhdGpzX1mukO76n-azClRI1VMmMbmo2xRpRmjehW_zBTFgyFfk-wGRdfQVN60LwOxE8DSCGrRNz_3S0003__mC0)

**Giải thích:**

### Applications Layer:
- **EmployeeActivities**: Bao gồm các hoạt động liên quan đến nhân viên như nhập thông tin thời gian làm việc, chọn phương thức thanh toán, v.v.
- **PayrollActivities**: Bao gồm các hoạt động liên quan đến việc xử lý lương bổng, tạo báo cáo lương, v.v.
- **Security**: Bao gồm các hoạt động bảo mật, xác thực và phân quyền.

### Business Services Layer:
- **PayrollService**: Cung cấp các dịch vụ liên quan đến việc xử lý lương bổng.
- **BankingService**: Cung cấp các dịch vụ liên quan đến giao dịch ngân hàng.
- **ReportingService**: Cung cấp các dịch vụ liên quan đến việc tạo và quản lý báo cáo.

### Database Layer:
- **EmployeeDatabase**: Lưu trữ thông tin về nhân viên.
- **PayrollDatabase**: Lưu trữ thông tin về các khoản lương và giao dịch liên quan.

### Mối quan hệ giữa các layers:
- **EmployeeActivities**, **PayrollActivities**, và **Security** trong **Applications Layer** phụ thuộc vào các dịch vụ trong **Business Services Layer**
- Các dịch vụ trong **Business Services Layer** phụ thuộc vào các cơ sở dữ liệu tương ứng trong **Database Layer**
