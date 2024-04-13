# clash for windows

```
# 参考链接：https://blog.csdn.net/AirenMc/article/details/75735152
# 只修改终端代理
# 在/etc/profile.d/proxy.sh下添加一个shell脚本文件，这将确保设置适用于所有已登录的用户：
sudo vim  /etc/profile.d/proxy.sh

# 将下列内容修改到文档中
# 其中ip地址替换为"http://电脑IP地址:7890/"
```

```
# set proxy config via profie.d - should apply for all users
export http_proxy="http://192.168.1.101:7890/"
export https_proxy="http://192.168.1.101:7890/"
export ftp_proxy="http://192.168.1.101:7890/"
export no_proxy="127.0.0.1,localhost"
# For curl
export HTTP_PROXY="http://192.168.1.101:7890/"
export HTTPS_PROXY="http://192.168.1.101:7890/"
export FTP_PROXY="http://192.168.1.101:7890/"
export NO_PROXY="127.0.0.1,localhost"
#将要从代理中排除的其他IP添加到NO_PROXY和no_proxy环境变量中
```

```
# 为该文件填加执行权限
sudo chmod +x  /etc/profile.d/proxy.sh

# 激活文件以开始使用代理设置，或者注销并重新登录
source /etc/profile.d/proxy.sh
#查看环境变量进行确认是否生效
env | grep -i proxy
```
