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

使用 `git checkout`命令回退到那个版本。你只需要把 `<commit_id>`替换为你找到的那个commit id。

```
git checkout 
```

如果你想要在回退后的版本上创建一个新的分支，你可以用以下命令

```
git checkout -b 
```

注意，使用 `git checkout`来回退版本会使你处于一个"detached HEAD"的状态。在这个状态下，如果你做了任何修改并commit，那么当你切换回原来的分支时，那些修改将会丢失。如果你想保留这些修改，你应该在 `git checkout <commit_id>`之后创建一个新的分支。

如果你想把你的HEAD和一个分支的tip都回退到之前的版本，并把后续的commit都删除，你可以使用 `git reset --hard <commit_id>`命令。请谨慎使用这个命令，因为这个操作是不可逆的，你将无法恢复删除的commit。

```
git reset --hard 
```
