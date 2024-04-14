# gitconfig

## git配置

```
# 配置git用户信息
git config --global user.name "Hao Lonpeng"
git config --global user.email "3518563454@qq.com"

# 给git配置本地clash 代理
git config --global http.proxy "socks5://127.0.0.1:7890"

# 重新生成git公钥
ssh-keygen -t rsa -C "3518563454@qq.com"

# 将id_rsa.pub复制到GitHub账户中
```

## git提交规范

```
<type>[optional scope]: <description>
# 空行
[optional body]
# 空行
[optional footer]
```

### type

`refactor` 表示本次提交的是**重构**代码，也就是它是一个提交的类型`type`，除了`refactor`还有：

-   `feat` 新功能，顾名思义就是新需求的实现。
-   `fix` 修复，就是对bug的修复。
-   `docs` 文档，主要用来描述文档的变更。
-   `style` 主要是代码风格相关的提交，比如格式化等。
-   `refactor` 重构代码，对已有功能的重构，但是区别于bugfix。
-   `test` 测试相关的提交，不太常用。
-   `chore` 构建过程或辅助工具的变动，不太常用，比如之前用Maven，后面换成了Gradle。

每次提交声明提交的`type`是必须的，它让本次提交的作用一目了然。

### scope（可选）

用来表明本次提交影响的范围，方便快速定位。你可以写明影响的是哪个模块（通常是模块名称）或者是哪个层（数据层、服务层、还是视图层）。

### subject

就是上面的`修改版权信息`，是对本次提交的简短描述概括。就像胖哥写文章要起一个标题一样，不要过长。

### body（可选）

就是比较详细描述本次提交涉及的条目，罗列代码功能，这里胖哥习惯用**markdown**的列表语法，也就是用中划线换行隔开条目。当然`body`不是必选的，如果`subject`能够描述清楚的话。

### foot（可选）

描述与本次提交相关联的**break change**或**issue** 。

#### break change

指明本次提交是否产生了破坏性修改，类似版本升级、接口参数减少、接口删除、迁移等。如果产生了上述的影响强烈建议在提交信息中写明**break change**，有利于出问题时快速定位，回滚，复盘。
