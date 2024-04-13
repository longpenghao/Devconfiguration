# vimrc

```
# 一般只对当前用户修改vim配置，只需要在主目录下创建一个.vimrc文件即可
vim ~/.vimrc

# 将下列内容写入文件中
```

```
set number
set backspace=2
set cursorline
set mouse=a
set selection=exclusive
set selectmode=mouse,key
set showmatch


set tabstop=4
set shiftwidth=4
set autoindent

set paste

set ruler


set enc=utf-8
set fencs=utf-8,ucs-bom,shift-jis,gb18030,gbk,gb2312,cp936

set langmenu=zh_CN.UTF-8
set helplang=cn

syntax enable

"设置字体"
"set guifont=dejaVu\ Sans\ MONO\ 10
set guifont=Courier_New:h10:cANSI

"设置颜色"
"colorscheme desert

"高亮显示当前行"
set cursorline
hi cursorline guibg=#00ff00
hi CursorColumn guibg=#00ff00

set si

set noswapfile

```

