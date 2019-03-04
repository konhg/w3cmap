##在用git 向github提交代码时出现：
    error: RPC failed; result=22, HTTP code = 411
    fatal: The remote end hung up unexpectedly

可能原因为HTTP缓存小于要更新的文件大小,修改HTTP缓存大小可解决问题:

```
git config http.postBuffer 524288000

```

##git 修改提交方式
git 提供两种提交方式

*   `http`方式,格式为:https:/gitlocate/xxx/xxx.git
*   `ssh`方式,格式为:git@gitlocate:x/xxx.git

如果要修改提交方式的话,可以在工程目录下的配置文件中修改:

```

vi  .../.git/config

#更新以下配置

url=http方式,或者ssh方式

```

## git 配置文件忽略

```
#如果不存在则新建一个文件,文件内按行添加过滤规则
vi .gitignore

``

如果要过滤的文件已经存在于版本库上,编辑后旧文件不会被识别出来,按照如下操作可使规则生效:

```
git rm -r --cached .
git add .
git commit
```

## git 配置数状展示

```
git config --global alias.tree "log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset'"

```
