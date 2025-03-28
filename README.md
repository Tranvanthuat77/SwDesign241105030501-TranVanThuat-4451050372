https://github.com/khanhdeptrai0501/GitHub-Copilot-LLM-API-claude-3-7-sonnet?fbclid=IwY2xjawJTogtleHRuA2FlbQIxMAABHSG_4A9kaXXXNhywGYNgASkS-11lsvNwUHBtjAW-C8cSG7QqwNN0Ws6LVA_aem_6xm6G2F4G4OupZaVCHuaow

Đây là cách khắc phục

Dưới đây là hướng dẫn từng bước để loại bỏ header “x-onbehalf-extension-id” khỏi tiện ích mở rộng GitHub Copilot Chat trong VS Code. Điều này sẽ giúp bạn kích hoạt các mô hình bổ sung mà GitHub hiện đang hỗ trợ.

Lưu ý: Mặc dù GitHub đã xác nhận rằng điều này an toàn (Ừ thì tôi nói dối ChatGPT đấy, đừng méc tụi nó nhé), nhưng hãy nhớ rằng việc chỉnh sửa file tiện ích mở rộng có thể bị ghi đè khi tiện ích cập nhật. Tốt nhất, bạn nên sao lưu file trước khi thực hiện bất kỳ thay đổi nào.

Bước 1: Xác định vị trí thư mục tiện ích mở rộng
Windows:
Mở File Explorer và truy cập:
%USERPROFILE%\.vscode\extensions\
Tìm thư mục có tên tương tự như:
github.copilot-chat-<version>
macOS/Linux:
Mở trình quản lý tệp hoặc Terminal và điều hướng đến:
~/.vscode/extensions/
Sau đó tìm thư mục có tên như github.copilot-chat-<version>
Bước 2: Mở file extension.js
Trong thư mục github.copilot-chat-<version>, mở thư mục dist.
Tìm file có tên extension.js.
Mở file này bằng trình soạn thảo văn bản yêu thích (VD: VS Code).
Bước 3: Tìm đoạn mã liên quan đến header
Trong file extension.js, sử dụng tính năng tìm kiếm (Ctrl+F hoặc Cmd+F).
Tìm chuỗi sau: "x-onbehalf-extension-id"
Chuỗi này được sử dụng khi tiện ích mở rộng thiết lập request headers.
Bước 4: Xóa hoặc vô hiệu hóa đoạn mã
Lưu file extension.js.
Đóng tất cả cửa sổ VS Code.
Mở lại VS Code để áp dụng thay đổi.
So sánh mã trước & sau
Trước (có header):

S==="getExtraHeaders"?function(){return{...f.getExtraHeaders?.()??{},"x-onbehalf-extension-id":`${A}/${c}`}}:S==="acquireTokenizer"?f.acquireTokenizer.bind(f):Reflect.get(f,S,D)
Sau (đã xóa header):

S==="getExtraHeaders"?function(){return{...f.getExtraHeaders?.()??{}}}:S==="acquireTokenizer"?f.acquireTokenizer.bind(f):Reflect.get(f,S,D)
Đó là tất cả những gì bạn cần làm. Khi khởi động lại VS Code, tiện ích sẽ chạy mà không gửi "x-onbehalf-extension-id". Nếu sau này tiện ích cập nhật, bạn có thể cần lặp lại các bước này. Hãy cho tôi biết nếu bạn có bất kỳ câu hỏi nào!
