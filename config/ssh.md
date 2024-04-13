## SSH设置
```
# 参考链接1：https://zhuanlan.zhihu.com/p/653975920
# 参考链接2：https://blog.csdn.net/AirenMc/article/details/75735152
# 给虚拟机安装ssh服务
sudo apt-get install openssh-server
sudo /etc/init.d/ssh restart
# ssh成功后会提示：[ ok ] Starting ssh (via systemctl): ssh.service.

# 验证ssh是否开启
ps -e|grep ssh
# 有如下类似结果即为开启
    826 ?        00:00:00 sshd
   4633 ?        00:00:00 sshd
   4668 ?        00:00:00 sshd

# 可能需要安装
sudo apt install openssh-client
```
```
# 回车多次，进行无密码登录
ssh-keygen -t rsa

# 使用“-f”制定保存密钥的文件名
ssh-keygen -t rsa -f “文件名称”
```
```
# 在.ssh文件夹下创建config文件
# 服务器名称
# 服务器IP地址
# 用户名
# 私钥在本地电脑的位置，使用~表示本地用户文件目录
Host   s1
    HostName        10.201.153.204
    Port            22
    User            hlp
    IdentityFile    ~/.ssh/id_rsa

# 附加：允许远程服务器上的图形应用程序接口显示在本地计算机上的功能
Host   se22
    HostName        192.168.64.131
    Port            22
    User            googbox
    IdentityFile    ~/.ssh/id_rsa
    ForwardX11 yes
    ForwardX11Trusted yes
```

```
# 如果服务器上没有文件夹.ssh和文件id_rsa.pub可能会复制不成功
# 创建文件夹和文件的方法如下：
# 创建文件夹.ssh
mkdir .ssh
# 进入对应目录
cd .ssh
# 创建文件id_rsa.pub
vim id_rsa.pub
```

```
# 将本地公钥id_rsa.pub文件复制到服务器
scp C:/Users/hao/.ssh/id_rsa.pub s1:~/.ssh
```

```
# 进入到.ssh文件夹下，如果没有authorized_keys文件，创建该文件
# 将服务器上的id_rsa.pub文件，复制到authorized_keys文件中：
cat id_rsa.pub > authorized_keys
chmod 600 ~/.ssh/authorized_keys
chmod 700 ~/.ssh
```

```
# 使用如下语句进入对应目录,打开sshd_config文件
cd /etc/ssh

# 使用如下语句打开文件sshd_config：
vim sshd_config

# 确认如下参数是yes，保证服务器当前用户可以密码登录
PasswordAuthentication yes
```

```
# xfce4
echo xfce4-session > ~/.xsession
```

```
sudo adduser 
sudo usermod -G 
```



