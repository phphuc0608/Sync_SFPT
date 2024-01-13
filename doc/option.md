# option command
Hiển thị hoặc đặt giá trị của các tùy chọn của script.
# Syntax
```
option [ <option> [ <value> ] ]
```
# Remarks
Nếu không có tham số nào được chỉ định, hãy liệt kê tất cả các tùy chọn của script và giá trị của chúng. Khi chỉ có một tham số được chỉ định, sẽ hiển thị giá trị của tùy chọn. Khi hai tham số được chỉ định, đặt giá trị của tùy chọn (sets value of option).<br>
Giá trị mặc định được hiển thị ở bên dưới là mặc định dành cho ứng dụng. Giá trị ban đầu của một số tùy chọn có thể khác nếu bạn [chia sẻ cấu hình với chế độ đồ họa](https://winscp.net/eng/docs/scripting#configuration).
Các lựa chọn bao gồm:
|Option|Values and description|
|:-----|:---------------------|
|`echo`|`off`, `on`<br>Chuyển đổi echoing của lệnh đang được thực thi.<br>Các command bị ảnh hưởng: tất cả<br> Mặc định: `off`|
|`batch`|`on`, `off`, `abort`, `continue`<br>Enables chế độ batch. Ở chế độ batch, mọi prompt lựa chọn sẽ tự động được trả lời và mọi input prompt đều bị hủy (sau khoảng thời gian ngắn).<br> Ở chế độ batch, ta nên đặt [confirm](https://winscp.net/eng/docs/scriptcommand_option#confirm) thành `off` để cho phép ghi đè.<br> Khi chế độ batch được đặt thành `on` bất kỳ prompt lựa chọn nào sẽ tự động được replied negatively. Trừ khi prompt có các câu trả lời mặc định khác nhau (ví dụ như câu trả lời mặc định dành cho reconnect prompt là "Reconnect"), trong trường hợp đó câu trả lời mặc định sẽ được sử dụng (sau một khoảng thời gian ngắn). Hãy xem [reconnecttime](https://winscp.net/eng/docs/scriptcommand_option#reconnecttime) ở bên dưới.<br>Giá trị `abort` giống như `on`. Ngoài ra, script bị hủy khi bất kỳ script command nào bị lỗi hoặc bất kỳ prompt lựa chọn nào được trả lời bằng câu trả lời "Abort" (hoặc tương tự).<br> Khi |
|||

