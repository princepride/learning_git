# learning_git

打印当前分支和所有分支

```
git branch
```

新建分支

```
git branch feature
```

切换分支

```
git checkout feature
```

分支合并（在主分支下）

```
git merge feature
```

命令用于将名为 "feature" 的分支的所有更改压缩为一个单独的提交。执行 `git merge --squash` 命令，这会将 "feature" 分支的所有更改应用到当前的工作目录，并在你的 Git 状态中显示它们是待提交的。然后，你需要创建一个新的提交，包含所有这些更改：git commit-m "Your commit message"

```
git merge --squash feature
```
