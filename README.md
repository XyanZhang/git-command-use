# myFirstTest

Learning how to use git commands

## git rebase

## git cherry-pick

假设有两个分支：feature和master，并且你想要将feature分支上的一个提交应用到master分支上。以下是具体步骤：

首先，切换到master分支：git checkout master
运行git log命令查看要应用的提交的SHA值（例如：commit-A）。
执行git cherry-pick commit-A命令，将feature分支上的commit-A应用到master分支上。此时会创建一个新的提交，包含commit-A的更改。
如果存在多个提交需要应用，按照相同的步骤重复执行即可。
