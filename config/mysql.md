# Ubuntu安装mysql

```
# 参考链接1：https://www.51cto.com/article/718700.html
# 参考链接2：https://www.cnblogs.com/2020javamianshibaodian/p/12920243.html
# 问题参考链接1：https://www.cnblogs.com/baby123/p/12221405.html
```

```
# 安装mysql
sudo apt update
sudo apt install mysql-server

# 验证mysql正在运行：
sudo systemctl status mysql
# 验证结果：
● mysql.service - MySQL Community Server
 Loaded: loaded (/lib/systemd/system/mysql.service; enabled; vendor preset: enabled)
 Active: active (running) since Tue 2020-04-28 20:59:52 UTC; 10min ago
 Main PID: 8617 (mysqld)
 Status: "Server is operational"
 ...
```

```
# 安装一个名为mysql_secure_installation的实用脚本
sudo mysql_secure_installation

# 安装过程中一直选择y
# 具体选择可以根据链接：https://www.cnblogs.com/baby123/p/12221405.html

# 对脚本进行设置
# 进入mysql服务
sudo mysql

# 查看mysql初始的密码策略
SHOW VARIABLES LIKE 'validate_password%';

# 修改初始密码策略,将强度设为弱
set global validate_password.policy=LOW;

# 设置root用户的密码
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'your_password';
FLUSH PRIVILEGES;

# 创建一个新用户，并授予该用户适当的权限
CREATE USER 'test1'@'localhost' IDENTIFIED BY 'your_password';
GRANT ALL PRIVILEGES ON *.* TO 'PyDataStudio'@'localhost' WITH GRANT OPTION;
```

```
# 登录方式
# root用户
mysql -u root -p
# 其他用户
mysql -u test1 -p
```
