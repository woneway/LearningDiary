常用命令：
## 如何将github项目关联本地已有文件夹
1. 从github新建一个项目(git@github.com:username/projectname.git)
2. 本地项目初始化，执行命令
```
git init
```
3. 关联远程仓库
```
git remote add origin git@github.com:username/projectname.git
```
4. 拉取远程仓库信息
```
git pull origin master
```
若该操作存在冲突，即报错
```
 * branch            master     -> FETCH_HEAD
fatal: refusing to merge unrelated histories
```
检查后没问题,则执行如下命令
```
git pull origin master --allow-unrelated-histories
```


## 克隆远程项目信息
```
git clone git@github.com:username/projectname.git
```


## 首次上传到远程仓库
origin是远程仓库地址，第一个master是本地仓库分支，第二个master是远程仓库分支
```
git push origin master:master
```
例如将本地master分支提交到远程仓库分支slave上，若slave不存在，则会新建一个slave分支
```
git push origin master:slave
```

## 删除远程分支
```
git push origin --delete ${deletebranchname}
```

## gitbash 展示中文为乱码
```
git config --global core.quotepath false
```