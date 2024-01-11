# Syntax
```
synchronize local|remote|both [ <local directory> [ <remote directory> ] ]
```
# Remarks
- Nếu như parameter đầu tiên là `local`, các thay đổi từ thư mục **remote** sẽ được áp dụng vào thư mục **local**.
- Nếu như parameter đầu tiên là `remote`, các thay đổi từ thư mục **local** sẽ được áp dụng vào thư mục **remote**.
- Nếu như parameter đầu tiên là `both`, cả hai thư mục đều có thể được sửa đổi.<br>
Khi mà các thư mục không được chỉ định thì tức là các thư mục đã được đồng bộ hóa.<br>
***Lưu ý***: Việc xác nhận ghi đè sẽ luôn được tắt cho command
## Switches:
|Switch|Description|
|:-----------|:-----------|
|`-preview`| xem trước các thay đổi, không đồng bộ hóa. Các cài đặt transfer chuyển đổi [`-permission`](https://winscp.net/eng/docs/scriptcommand_synchronize#permissions), [`-nopermissions`](https://winscp.net/eng/docs/scriptcommand_synchronize#nopermissions), [`-speed`](https://winscp.net/eng/docs/scriptcommand_synchronize#speed), [`-transfer`](https://winscp.net/eng/docs/scriptcommand_synchronize#transfer) và [`-resumesupport`](https://winscp.net/eng/docs/scriptcommand_synchronize#resumesupport) sẽ không có tác dụng|
|`-delete`|Xóa các files đã lỗi thời (obsolete). Ignore ở chế độ `both`|
|`-mirror`|[Mirror mode](https://winscp.net/eng/docs/task_synchronize_full#mode) (đồng bộ cả với file cũ hơn). Ignore ở chế độ `both`|
|`-criteria=<criteria>`|[Comparison criteria](https://winscp.net/eng/docs/ui_synchronize#criteria). Ở phiên bản stable mới nhất, các values có thể là `time`, `size`, `either` và `none`. Ở phiên bản thử nghiệm, các values có thể là `time`, `size` và `checksum`, hoặc `none`. Ignore ở chế độ `both`|
|`-preservetime`|Giữ lại timestamp. Thực thi theo mặc định trừ khi [`-criteria`](https://winscp.net/eng/docs/scriptcommand_synchronize#criteria) thiếu giá trị `time`|
|`-nopreservetime`|Không giữ lại timestamp. Nó sẽ ignore trừ khi [`-criteria`](https://winscp.net/eng/docs/scriptcommand_synchronize#criteria) thiếu giá trị `time`|
|`-permissions=<mode>`|Set quyền (chỉ với giao thức [SFTP](https://winscp.net/eng/docs/sftp) và [SCP](https://winscp.net/eng/docs/scp))|
|`-nopermissions`|Giữ nguyên quyền mặc định|
|`-speed=<kbps>`|Giới hạn tốc độ transfer (KB/s)|
|`-transfer=<mode>`|`binary`, `ascii`, `automatic`<br>[Transfer mode](https://winscp.net/eng/docs/transfer_mode): binary, ascii(text), automatic(by extension)|
|`-filemask=<mask>`|`<mask>[;<mask2>...]`<br> Sets [file mask](https://winscp.net/eng/docs/file_mask)|
|`resumesupport=<state>`|`on`,`off`,`<threshold>`<br>Cấu hình [tự động resume / chuyển sang filename tạm thời](https://winscp.net/eng/docs/resume#automatic).|
|`-rawtransfersettings setting1=value1 setting2=value2 …`|Cho phép cấu hình mọi cài đặt transfer bằng định dạng thô như trong tệp INI. Ví dụ. để cho phép lưu timestamp của thư mục, hãy sử dụng `-rawtransfersettings PreserveTimeDirs=1`. Switch chỉ nên đến sau các thông số khác.|