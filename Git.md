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
