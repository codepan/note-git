# github远程仓库地址种类
github远程仓库地址有两种形式：
* https地址：https://github.com/codepan/note-git.git
* ssh地址：git@github.com:codepan/note-git.git

当使用https地址与远程仓库建立连接，`git remote add origin <https>`不需要生成公钥和私钥

但如果使用ssh地址与远程仓库建立连接时github会强制要求您需要在本地生成公钥和私钥，然后将公钥添加至github仓库中，这样本地git仓库才能正常的与远程git仓库进行数据交换

# 生成ssh公钥私钥

存放目录
* Mac电脑：`~/.ssh`
* Windows电脑：`不知道`

生成所使用的命令：`ssh-keygen`，该命令存在于`/usr/bin/ssh-keygen`这个目录下，该命令是Mac或Linux系统自带的。在Windows系统中可以下载一个叫做`putty`的工具，其提供了ssh全套的命令可供使用

```bash
# 生成
ssh-keygen
# 回车
# 回车
# 经过三次回车之后，就会生成公钥和私钥
```

# 将生成的公钥添加至github仓库中
```bash
cd ~/.ssh
vi id_rsa.pub
```
复制这个文件中的内容

* 仓库级别添加公钥

    然后点击github仓库中的 Settings，然后点击左侧的 Deploy keys，然后点击右侧的 Add deploy key，然后输入 Title，然后将刚才复制的内容粘贴到Key这个文本域中，然后勾选上 Allow write access选项，最后点击 Add key按钮，至此成功增加了公钥到github仓库中

* github账号级别添加公钥

  点击github右上角最右边的图标，然后点击 Settings，然后点击左侧的 SSH and GPG keys，然后点击 New SSH key，然后输入 Title，然后将刚才复制的内容粘贴到Key这个文本域中，最后点击 Add SSH key按钮，完成github账号级别的
