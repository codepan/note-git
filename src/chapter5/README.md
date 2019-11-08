# 删除文件 (git rm)
```shell
git rm <file|directory|.>
```
删除xxx文件，版本库和工作区都会一并被删除

```shell
git rm -—cached <file|directory|.>
```
从缓存区中删除被add的文件，或者从版本库中删除被commit的文件，将文件放回工作区
