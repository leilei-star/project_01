# Git命令

## 1.仓库初始化

``` shell
git inot  #title  ## 一级标题  ``` 阴影框
```

## 2.添加到暂存区

```shell
git add 文件名  
git add . 把新建的和修改的内容都添加到暂存区
```

## 3.提交到Git库

```shell
git commit -m "初始化..."
```

## 4.查看状态

```shell
git status  shell
```

```shell
git status -s
```

## 5.撤销

```shell
git checkout --文件名
```

## 6.移除暂存区里面的内容

```shell
git reset HEAD 文件名 
git reset HEAD . 移除所有
```

## 7.移除wenjain

```shell
1：从Git仓库和工作区一块删除 
git rm -f 文件名
2：从git仓库删除 工作区保留
git rm --cached 文件名
```

## 8.忽略文件

```shell
① 以 # 开头的是注释

② 以 / 结尾的是目录

③ 以 / 开头防止递归

④ 以 ! 开头表示取反

```

## 9.查看提交历史

```shell
# 按时间先后顺序列出所有的提交历史，最近的提交在最上面
git log

# 只展示最新的两条提交历史，数字可以按需进行填写
git log -2

# 在一行上展示最近两条提交历史的信息
git log -2 --pretty=oneline

# 在一行上展示最近两条提交历史信息，并自定义输出的格式
# &h 提交的简写哈希值  %an 作者名字  %ar 作者修订日志  %s 提交说明
git log -2 --pretty=format:"%h | %an | %ar | %s"
```

## 10.回退到指定的版本

```shell
# 在一行上展示所有的提交历史
git log --pretty=oneline

# 使用 git reset --hard 命令，根据指定的提交 ID 回退到指定版本
git reset --hard <CommitID>

# 在旧版本中使用 git reflog --pretty=oneline 命令，查看命令操作的历史
git reflog --pretty=onelone

# 再次根据最新的提交 ID，跳转到最新的版本
git reset --hard <CommitID>
```

