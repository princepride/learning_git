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


用于将你的本地代码推送到GitHub或其他托管Git代码的远程仓库。下面是详细解释：

* `git push`： 这是基础的git命令，用于将你本地仓库的变更推送到远程仓库。
* `--set-upstream`： 这个参数用于设置远程跟踪分支。当设置后，未来只需使用 `git push` 或 `git pull` 命令，Git 就会知道你希望与哪个分支进行交互。
* `origin`： 通常，origin 是你克隆远程仓库时自动设置的默认名称。它代表了原始的远程仓库地址。
* `shopee2`： 这是你要推送的本地分支的名称。

总结一下，这条命令的意思就是“将本地的 'shopee2' 分支推送到名为 'origin' 的远程仓库，并设置 'origin' 的 'shopee2' 分支作为 'shopee2' 分支的上游（即默认远程分支）。” 如果远程 'origin' 仓库不存在 'shopee2' 分支，那么将会创建一个。

```
git push --set-upstream origin shopee2
```
