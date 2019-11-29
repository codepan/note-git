# 标签 (git tag)
发布一个系统，或者系统到达某一个里程碑的时候，最需要打一个tag，做一个标记

标签不是专属于某一个分支的，换言之：标签和分支是没有关系的，标签属于整个git仓库，标签不会随着分支的切换而改变。

标签有两种
* 轻量级标签（lightweight）
* 带有附注标签（annotated）

```bash
# 查看标签列表
git tag

# 新建一个tag在当前commit
# eg: git tag v1.0.0
git tag [tag]

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