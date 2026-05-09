## 安装git

[下载 git Mac 版](http://git-scm.com/download/mac)

[下载 git Windows 版](http://msysgit.github.io/)

[下载 git Linux 版](http://git-scm.com/download/linux)

## Git 教程

许多人认为 Git 太混乱，或认为它是一种复杂的版本控制系统，其实不然，这篇文章有助于大家快速上手使用 Git。

![](https://www.runoob.com/wp-content/uploads/2015/02/git.jpg)

## 入门

使用Git前，需要先建立一个仓库(repository)。您可以使用一个已经存在的目录作为Git仓库或创建一个空目录。

使用您当前目录作为Git仓库，我们只需使它初始化。

```sh
git init
```

使用我们指定目录作为Git仓库。

```sh
git init newrepo
```

从现在开始，我们将假设您在Git仓库根目录下，除非另有说明。

### 添加新文件

我们有一个仓库，但什么也没有，可以使用add命令添加文件。

```sh
git add filename
```

可以使用add... 继续添加任务文件。

### 提交版本

现在我们已经添加了这些文件，我们希望它们能够真正被保存在Git仓库。

为此，我们将它们提交到仓库。

```sh
git commit -m "Adding files"
```

如果您不使用-m，会出现编辑器来让你写自己的注释信息。

当我们修改了很多文件，而不想每一个都add，想commit自动来提交本地修改，我们可以使用-a标识。

```sh
git commit -a -m "Changed some files"
```

git commit 命令的-a选项可将所有**被修改或者已删除的且已经被git管理的文档**提交到仓库中。

千万注意，-a不会造成新文件被提交，只能修改。

### 发布版本

我们先从服务器克隆一个库并上传。

```sh
git clone ssh://example.com/~/www/project.git
```

现在我们修改之后可以进行推送到服务器。

```sh
git push ssh://example.com/~/www/project.git
```



### 取回更新

如果您已经按上面的进行push，下面命令表示，当前分支自动与唯一一个追踪分支进行合并。

```sh
git pull
```

从非默认位置更新到指定的url。

```sh
git pull http://git.example.com/project.git
```



## 已经超过了五分钟？

### 删除

如何你想从资源库中删除文件，我们使用rm。

```sh
git rm file
```



### 分支与合并

分支在本地完成，速度快。要创建一个新的分支，我们使用branch命令。

```sh
git branch test
```

branch命令不会将我们带入分支，只是创建一个新分支。所以我们使用checkout命令来更改分支。

```sh
git checkout test
```

第一个分支，或主分支，被称为"master"。

```sh
git checkout master
```

对其他分支的更改不会反映在主分支上。如果想将更改提交到主分支，则需切换回master分支，然后使用合并。

```sh
git checkout master
git merge test
```

如果您想删除分支，我们使用-d标识。

```sh
git branch -d test
```
## 相关文章

- Github 简明教程：[http://www.runoob.com/w3cnote/git-guide.html](https://www.runoob.com/w3cnote/git-guide.html)
- Git 教程：[http://www.runoob.com/git/git-tutorial.html](https://www.runoob.com/git/git-tutorial.html)