# zshrc

```
# 参考链接：https://zhuanlan.zhihu.com/p/441676276
# 查看当前shell
echo $SHELL
# 查看当前可用的shell
cat /etc/shells

# 安装zsh，并将它替换为默认zsh
sudo apt install zsh -y
chsh -s /bin/zsh
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

```
# 安装插件zsh-autosuggestions，命令行键入提示
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

# 安装插件zsh-syntax-highlighting，命令语法校验插件
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
# 备用
git clone https://gitee.com/Annihilater/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting

# 主题选择
# 参考链接：https://github.com/romkatv/powerlevel10k
```

```
# zsh配置修改
# 修改.zshrc中的内容
vim .zshrc

# 修改下述内容
ZSH_THEME="crcandy"
plugins=(git  zsh-autosuggestions zsh-syntax-highlighting )

# 重新启动zsh
source ~/.zshrc
```
