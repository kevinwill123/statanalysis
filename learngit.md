### learngit

1.创建目录

```
mkdir learngit
cd learngit
pwd #显示当前目录名称
```

2.初始化目录为git可管理的仓库

```
git init
```

3.添加文档

```
git add filename.typename
```

4.执行git操作

```
git commit -m "message" #-m后一般是对操作内容的描述
```

5.查看git日志

```
git log
git log --pretty=oneline #可以美化日志展示的形式
```

6.版本回溯

```
git reset HEAD #表示当前版本
git reset HEAD^ #表示上一个版本
git reset HEAD^^ #表示上上个版本
git reset HEAD-100 #表示之前的第100个的版本
git reset --hard commint_id #commit_id是版本号的前几个字符
git reflog #回退版本后再回到未来/现在的版本
```

7.状态查询

```
工作区：本地可以看到的文件夹内容
版本库：工作区中的隐藏部分。其中有一部分是暂存区。
git status 查看git状态
```

8.管理修改

```
cat <file>

git diff HEAD -- readme.txt #查看工作区和版本库里最新版本的区别
```

9.撤销修改

```
git checkout -- <file>
```

10.删除文件

```
rm <file> 这时候git已经知道了我们已经删除了file

- git rm <file> #在git仓库中删除这个文件
- git checkout -- <file> #将误删的文件恢复到版本库里的最新版本
```

**git checkout其实是用版本库里的版本替换工作区的版本，无论工作区是修改还是删除，都可以“一键还原”**


11.添加远程仓库

create a new repo -> 填写reposititory name
-> git remote add origin git@github.com:<github_username>/learngit.git

12.推库

```
git push -u origin master

git push origin master #第一次初始化推送以后我们就可以使用这条命令同步本地库和远程库
```


*因为文件已经传输成功 这部分的简单基础入门学习也就完成了*
