- Script file (.txt)
```
# Connect to SFTP server using a password
open sftp://username:password@IP:port/ -hostkey="ssh-rsa 1024 ...."
# Synchronize
synchronize local|remote|both "local_dir" "remote_dir"
# Exit WinSCP
exit
```
- Run file (.bat)
```
#path of execute_file -> path of script_file -> path of log file
"path_of_execute_file" /console /script="path_of_script" > "path_of_log"
```
# Command
## Synchronize command
### Switches:
|Switch|Description|
|:-----------|:-----------|
|`-preview`| Xem trước các thay đổi, không đồng bộ hóa. Các cài đặt transfer chuyển đổi [`-permission`](https://winscp.net/eng/docs/scriptcommand_synchronize#permissions), [`-nopermissions`](https://winscp.net/eng/docs/scriptcommand_synchronize#nopermissions), [`-speed`](https://winscp.net/eng/docs/scriptcommand_synchronize#speed), [`-transfer`](https://winscp.net/eng/docs/scriptcommand_synchronize#transfer) và [`-resumesupport`](https://winscp.net/eng/docs/scriptcommand_synchronize#resumesupport) sẽ không có tác dụng|
