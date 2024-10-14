# <span style="color: #2E8B57;">I Lab 0 - Biểu đồ lớp</span>
========================================================================

***Dưới đây là biểu đồ lớp cho các đối tượng `Dwelling`, `Apartment`, `House`, và `Commune` được tạo bằng PlantUML.***

========================================================================

<div align="center">
  <img src="https://www.planttext.com/api/plantuml/png/D8un3i8m34Ltdy8Z3DoXg0mWiJD7ZLLPJMmKEtH0d8o18t45WWBRUyFN--_dQp0FnMjE0BQmO54Z06TFX6CAPcIuwuG73dC96G2cxYkbn3BZ7H3n98uNbgYhVVMc7F6iqxBPmkE_s5zRB9FupuzQMwxpg3bNQV619BP37m000F__0m00" alt="Activity Diagram">
</div>

## <span style="color: #4682B4;">Mô tả sơ đồ lớp</span>

Sơ đồ lớp này mô tả cấu trúc của các đối tượng trong một hệ thống liên quan đến nhà ở, với các lớp chính như sau:

1. **Dwelling**:
   - **Lớp cha** (Superclass) trong sơ đồ, đại diện cho một dạng cư trú chung. 
   - **Các thuộc tính**:
     - `Windows`: Số lượng cửa sổ của nơi cư trú, kiểu dữ liệu là `Int`.
   - **Phương thức**:
     - `Lock()`: Một phương thức để khóa nơi cư trú, không trả về giá trị (void).

2. **Apartment**:
   - **Lớp con** (Subclass) kế thừa từ lớp `Dwelling`.
   - Đại diện cho các căn hộ, có thể có các thuộc tính và phương thức riêng nhưng không được liệt kê trong sơ đồ.

3. **House**:
   - **Lớp con** (Subclass) khác kế thừa từ lớp `Dwelling`.
   - Đại diện cho các ngôi nhà, cũng có thể có các thuộc tính và phương thức riêng.

4. **Commune**:
   - **Lớp con** (Subclass) thứ ba kế thừa từ lớp `Dwelling`.
   - Đại diện cho các cộng đồng cư trú hoặc khu dân cư, tương tự như hai lớp con trên.

### <span style="color: #8B4513;">Tổng quan:</span>
Sơ đồ này thể hiện mối quan hệ giữa các lớp trong hệ thống, trong đó `Dwelling` là lớp cơ sở và các lớp con (`Apartment`, `House`, `Commune`) kế thừa các thuộc tính và phương thức của lớp `Dwelling`. Điều này cho phép việc tổ chức và quản lý thông tin liên quan đến các loại nơi cư trú khác nhau trong hệ thống một cách dễ dàng và hiệu quả.

---

# <span style="color: #2E8B57;">II Lab 0 - Use Case Diagram</span>
================================================================

***Dưới đây là sơ đồ **Use Case** mô tả các hành động mà người dùng có thể thực hiện trong hệ thống:***

================================================================

<div align="center">
  <img src="https://www.planttext.com/api/plantuml/png/UhzxFnUNGt59Ob59QMuE5rTnTcQUGb5-SIeNLqbcIKwgGcXnge9p8f1moKnCBqhCLU3YujBmoK_FpDFaqWWgpLC8ACfFJYqkrbH8B5RG074CDRbAYrEJGNeqGlDIyk4g4C90_Gh-fILWFQ7E9a0NfEQb0Eq70000__y30000" alt="Use Case Diagram">
</div>

## <span style="color: #4682B4;">Mô tả các trường hợp sử dụng</span>

1. **(Login)**:
   - Đây là trường hợp sử dụng mà người dùng cần thực hiện để đăng nhập vào hệ thống. Người dùng nhập thông tin đăng nhập (tên người dùng và mật khẩu) để xác thực.

2. **(Run Process)** (được đặt tên là **Proc1**):
   - Đây là trường hợp sử dụng mô tả việc thực thi một quy trình nào đó trong hệ thống. Quy trình này có thể là một hành động hoặc chuỗi hành động mà người dùng hoặc hệ thống thực hiện.

3. **(Undo Process)**:
   - Đây là trường hợp sử dụng mô tả khả năng hủy hoặc hoàn tác một quy trình đã thực hiện trước đó. Tính năng này giúp người dùng quay trở lại trạng thái trước của hệ thống.

4. **(Log Out)** (được đặt tên là **UC4**):
   - Trường hợp sử dụng này mô tả quá trình đăng xuất khỏi hệ thống, đảm bảo rằng phiên làm việc của người dùng được kết thúc một cách an toàn và bảo mật.

---

# <span style="color: #2E8B57;">III Lab 0 - Activity Diagram with Notes</span>
================================================================================

***Dưới đây là sơ đồ **Activity Diagram** mô tả quá trình "Eat Hot Wings" và "Drink Homebrew" kèm theo một ghi chú chi tiết.***

================================================================================

<div align="center">
  <img src="https://www.planttext.com/api/plantuml/png/D8un3i8m34Ltdy8Z3DoXg0mWiJD7ZLLPJMmKEtH0d8o18t45WWBRUyFN--_dQp0FnMjE0BQmO54Z06TFX6CAPcIuwuG73dC96G2cxYkbn3BZ7H3n98uNbgYhVVMc7F6iqxBPmkE_s5zRB9FupuzQMwxpg3bNQV619BP37m000F__0m00" alt="Activity Diagram">
</div>

## <span style="color: #4682B4;">Mô tả sơ đồ</span>

1. **Eat Hot Wings**:
   - Đây là hành động đầu tiên trong quy trình, mô tả việc ăn cánh gà cay.

2. **Ghi chú (Note)**:
   - Ghi chú chứa nhiều định dạng văn bản khác nhau:
     - Ghi chú gồm nhiều dòng văn bản.
     - Một dòng được in nghiêng bằng cú pháp *italics*.
     - Một dòng chứa thẻ HTML `<b>` để làm nổi bật chữ in đậm.
     - Có một dòng là danh sách dấu đầu dòng (bullet).
     - Một dòng văn bản được hiển thị dưới dạng khối mã (code block) để nhấn mạnh cú pháp.

3. **Drink Homebrew**:
   - Hành động tiếp theo là uống bia tự nấu sau khi ăn cánh gà cay.

4. **Kết thúc**:
   - Quy trình kết thúc sau khi uống bia.

---


