暂存区操作 (git stash)
```shell
# 储藏工作区，并未执行add，也未执行commit
git stash

# 查看储藏的工作区
git stash list

# 储藏工作区，并且编写备注
git stash save <remark>

# 恢复指定的储藏到工作区，但不删除储藏
git stash apply <stash>

# 删除指定的储藏
git stash drop <stash>

# 恢复指定的储藏到工作区，并删除储藏（这个命令相当于上面两条命令连用）
git stash pop
```