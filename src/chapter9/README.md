# 储藏工作区 (git stash)
使用场景为：在某一个分支上开发，但这时有另一个需求需要在另一个分支上进行开发，此时是无法直接切换到另一个分支上的，因为当前的分支所做的变更没有add，也没有commit，切换分支会导致本次的变更丢失掉。

该问题有两种解决办法：
* 当前分支上执行add和commit，进行提交（既不推荐，因为commit的代码我们认为应该是OK的，测试通过的，而写了一半的代码就执行commit，显然不合理，后期寻找问题做版本回退时也会非常麻烦）
* 储藏工作区（推荐）

```bash
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