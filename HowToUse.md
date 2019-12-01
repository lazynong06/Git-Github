## Git的三个区域概念

Git有工作区、暂存区和版本库的概念。

- 工作区：就是电脑能看到的目录；

- 暂存区：英文叫stage或index。一般存放在`.git`目录下的index文件中，所以我们把暂存区有时也叫作索引(index)。

- 版本库：工作区有一个隐藏目录`.git`，这个不算工作区，而是Git的版本库。

  ![avatar](https://www.runoob.com/wp-content/uploads/2015/02/1352126739_7909.jpg)

## Git的命令和操作

### 简单的操作

### git status

> 使用这个命令查看当前工作区的状态。

### git add  <file>

> 将修改后的文件添加至**暂存区**，等待commit。

### git commit -m "commit reason"

> 提交修改，-m代表添加信息，后面跟提交的原因，方便后期查看更新原因

### git log

> 查看更新日志

### git show commit_id

> 查看某次commit的详情，commit_id形如`0bd6e0e7d485f1a2946d1726f7ae6c8e4f2b8725`

### git config  --global user.email "xxxxx@xxx.com"

### git config --global user.name "name"

> 修改提交人的邮箱
>
> 修改提交人姓名

### git reset commit_id

> 将滚回commit_id状态，git log显示的日志中，最上面的是最近提交的。

### git push

> 将修改推向远端
>
> 当我们推向远端时，若远端有更新，就要先`git pull`，然后会对修改进行自动合并，若修改有冲突，则需要手动修改，然后才能进行push

### git pull

> 拉取远端的更新

### 团队协同操作

### git branch branchname

> 创建一个名为branchname的分支

### git checkout branchname

> 切换到branchname分支

### git checkout -b branchname

> 等价于上面两个操作的合并

### git push --set-upstream origin branchname

> 在远端创建一个branch并且将修改推到远端

### 进行项目合并

- 先切换到master分支
- git pull拉取当前分支的更新
- git merge branch1命令将branch1合并到master

### 使用IDEA进行GIt操作

