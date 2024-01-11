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
```bat
#path of execute_file -> path of script_file -> path of log file
"path_of_execute_file" /console /script="path_of_script" > "path_of_log"
```
# Command
## Synchronize command
### Switches:
+ `-mirror`: synchronize also older files. Ignore for `both` mode 
