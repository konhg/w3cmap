#新建分支范例

```
#1. 通过当前分支新建一个分支,且切换到新的分支
git checkout -b [branch]

#2. 将新分支推送到远程服务器上
git push origin [branch]

#3. 将当前分支绑定到远程分支上(以后执行 git push 命令将默认提交到远程的这个分支)
git branch --set-upstream-to=origin/[branch]
```

#合并分支范例

```
#1 将远程分支合并到本地当前分支
git merge origin/master

#2 切换到master分支
git checkout master
git pull

#3 将其他分支合并到master分支
git merge [branch]

#4 提交及推送分支
git commit
git push
```