# 标签 (git tag)
标签有两种
* 轻量级标签（lightweight）
* 带有附注标签（annotated）

```shell
# 查看标签列表
git tag

# 新建一个tag在当前commit
git tag [tag] # eg: git tag v1.0

# 新建一个tag在指定commit
git tag [tag] [commit]

# 新建一个带有附注的标签
git tag -a <tag> -m <remark>

# 模糊查找tag
git tag -l <keyword>

# 删除本地tag
git tag -d [tag]

# 删除远程tag
git push origin :refs/tags/[tag]

# 查看tag信息
git show [tag]

# 提交指定的tag
git push [remote] [tag]

# 提交所有tag
git push [remote] --tags

# 新建一个分支，指向某个tag
git checkout -b [branch] [tag]
```