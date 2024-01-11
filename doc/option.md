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
|`batch`|`on`, `off`, `abort`, `continue`<br>Enables chế độ batch. Ở chế độ batch, mọi lời nhắc lựa chọn sẽ tự động được trả lời và mọi input prompt đều bị hủy (sau khoảng thời gian ngắn).<br> Ở chế độ batch, ta nên đặt [confirm](https://winscp.net/eng/docs/scriptcommand_option#confirm) thành `off` để cho phép ghi đè|
|||

