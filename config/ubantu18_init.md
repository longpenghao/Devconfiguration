# ubantu18 init

## 基础命令安装

```bash
sudo apt install build-essential
sudo apt install vim
sudo apt-get install curl -y
sudo apt-get install git -y
sudo apt-get install net-tools -y
# sudo apt-get install open-vm-tools-desktop -y
```

* 配置on-my-zsh
    * `echo $SHELL`
    * `cat /etc/shells`
    * `sudo apt install zsh -y`
    * `chsh -s /bin/zsh`
    * `sudo reboot`
* 配置.vimrc
* 安装jdk8[link](https://blog.csdn.net/zbj18314469395/article/details/86064849)
    * `sudo apt-get install openjdk-8-jdk -y`
* 安装conda
    * `wget -c https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh`
    * `chmod 777 Miniconda3-latest-Linux-x86_64.sh`
* 安装vscode
    * `wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add -`
    * `sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main"`
    * `sudo apt update`
    * `sudo apt install code`
* 安装chrome
    * `wget -q -O - https://dl.google.com/linux/linux_signing_key.pub | sudo apt-key add -`
    * `sudo sh -c 'echo "deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google-chrome.list'`
    * `sudo apt update && sudo apt install google-chrome-stable`



* 卸载java-8
   * `sudo apt-get remove openjdk-8-jre-headless `
   * `sudo apt-get remove openjdk-8-jdk`
