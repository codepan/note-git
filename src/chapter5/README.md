# 删除文件 (git rm)
```bash
# 删除文件|目录|当前目录下的所有内容，并且会自动将被删除的内容纳入到暂存区
git rm <file|directory|.>

# 从缓存区中删除被add的文件，或者从版本库中删除被commit的文件，将文件放回工作区
git rm -—cached <file|directory|.>
```

# git rm与rm的区别

git rm 做了两件事情：
* 删除了一个内容
* 并且会自动将删除的内容纳入到暂存区

若想恢复被删除的文件，需要进行两个动作：
* `git reset HEAD <file>` 将被删除的文件从暂存区恢复到工作区
* `git checkout -- <file>` 将工作区的修改丢弃掉


rm仅仅只会将文件删除，不会纳入到暂存区