## Git的三个区域概念

Git有工作区、暂存区和版本库的概念。

- 工作区：就是电脑能看到的目录；

- 暂存区：英文叫stage或index。一般存放在`.git`目录下的index文件中，所以我们把暂存区有时也叫作索引(index)。

- 版本库：工作区有一个隐藏目录`.git`，这个不算工作区，而是Git的版本库。

  ![avatar](https://www.runoob.com/wp-content/uploads/2015/02/1352126739_7909.jpg)

## 将Git与远端连接

### 生成SSH Key
- 输入命令ssh-keygen -t rsa，会生成密钥文件，id_rsa.pub是公钥，密钥文件默认存在home/user/.git文件中
### 添加GitHub的SSH密钥
- 登录GitHub账户
- 打开Setting
- 找到SSH and GPG
- 选择SSH Keys
- 选择 New SSH Key
- 将id_ras.pub的内容粘贴到Key栏
### 检查是否配置成功
- 添加SSH Key后，输入命令ssh -T git@github.com查看是否配置成功

### 本地库与远端库连接
- 输入命令git remote add origin https://github.com/username/repo_name.git

## Git的命令和操作

### 简单的操作

### `git status`

> 使用这个命令查看当前工作区的状态。

### `git add  <file>`

> 将修改后的文件添加至**暂存区**，等待`commit`。

### `git commit -m "commit reason"`

> 提交修改，`-m`代表添加信息，后面跟提交的原因，方便后期查看更新原因

### `git log`

> 查看更新日志

### `git show commit_id`

> 查看某次`commit`的详情，`commit_id`形如`0bd6e0e7d485f1a2946d1726f7ae6c8e4f2b8725`

### `git config  --global user.email "xxxxx@xxx.com"`

### `git config --global user.name "name"`

> 修改提交人的邮箱
>
> 修改提交人姓名

### `git reset commit_id`

> 将滚回`commit_id`状态，git log显示的日志中，最上面的是最近提交的。

### `git push`

> 将修改推向远端
>
> 当我们推向远端时，若远端有更新，就要先`git pull`，然后会对修改进行自动合并，若修改有冲突，则需要手动修改，然后才能进行`push`

### `git pull`

> 拉取远端的更新

### 团队协同操作

### `git branch branchname`

> 创建一个名为`branchname`的分支

### `git checkout branchname`

> 切换到`branchname`分支

### `git checkout -b branchname`

> 等价于上面两个操作的合并

### `git push --set-upstream origin branchname`

> 在远端创建一个`branch`并且将修改推到远端

### 进行项目合并

- 先切换到`master`分支
- `git pull`拉取当前分支的更新
- `git merge branch1`命令将`branch1`合并到`master`

### 使用IDEA进行Git操作

