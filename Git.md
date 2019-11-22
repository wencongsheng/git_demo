#Git_Demo

## 基本命令

### 初始化仓库

```shell
git init 
```

### 拉取项目
```shell
git clone https://github.com/wencongsheng/git_demo.git
```

### 添加文件
```shell
git add .
```

### 提交文件
```shell
git commit -m "xxxx"
```
### 添加远程仓库
```shell
 git remote add origin https://github.com/wencongsheng/git_demo.git
```
### 提交到远程地址 master 分支
```shell
git push origin master
```
### 拉取代码
```shell
git pull
```

### git工作状态
```
git status
```

## 工作缓存区

### 工作缓存
```
git stash 
```

### 工作缓存列表
```
git stash list
```

### 还原工作缓存区
```
git stash pop stash@{0}
```

### 删除缓存区
```
git stash drop stash@{0}
```

### 清除缓存区
```shell
git stash clear
```

## 版本管理

### 查看日志
--pretty=oneline 美化日志输出

```
git log [--pretty=oneline] 
```

### 查看不同文件
```shell
git diff README.md
```

### 返回上一个版本 
[HEAD^^] 上上个 
HEAD~100 往上100个
```shell
git reset --hard HEAD^
```

### 指定版本
```shell
git reset --hard 1094a[commit id]
```

### 命令历史
```shell
git reflog
```

### 工作区文件恢复
```shell
git checkout -- README.md
```

### 暂存区的修改撤销掉unstage
```shell
git reset HEAD README.md
```

### 注意：从来没有被添加到版本库就被删除的文件，是无法恢复的！
### 删除文件 
```shell
git rm README.md  && git commit -m "rm README.md"
```

## 分支管理
### 创建分支 

```shell
git checkout -b dev
```
-b创建并切换，相当于以下两条命令
```
git branch dev
git checkout dev
```
### 查看当前分支 当前分支会标个*号
```shell
git branch
```

### 切换dev分支
```shell
git add .
git commit -m "dev"
git branch master // 切换回主分支，准备merge合并
```
### 合并分支
```
git merge dev

```
### 删除分支
```shell
git branch -d dev
```

### 创建并切换到新的dev分支
```shell
git switch -c dev
```
### 直接切换
```shell
git switch master
```

## 名词解释

### 工作区
电脑中能看到的目录

### 板本库
工作区有个隐藏目录.git, 这是git版本库

#### stage 暂存区
git add 把文件添加进去，就是把文件添加到暂存区
git commit 提交更改，把暂存区的所有内容提交到当前分支
#### master 分支
commit 提交的文件
#### master 的一个指针HEAD


#### add 与commit 
commit 只会提交已经add的文件
