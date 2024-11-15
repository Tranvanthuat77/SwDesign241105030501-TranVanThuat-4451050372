# Lab 3. Identify Design Elements

## 1. Xác định các phần tử thiết kế của hệ thống “Payroll System”

### Subsystem Context Diagrams

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

![Mapping Analysis Classes to Design Elements - Login](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3bToJc9niOAIqyDTY_FI5GutvcKeH3pSjL319pyzCqz98R5OmJUne20pBpqaCIadrLYXcai126eKV1x
