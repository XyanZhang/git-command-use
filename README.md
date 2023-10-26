# myFirstTest

Learning how to use git commands

## git rebase

git rebase和git merge是两种不同的分支合并策略，它们有以下区别：

Commit历史：当使用git merge时，合并后的提交历史将保留源分支和目标分支的独立提交，并且会创建一个新的合并提交来表示合并的结果。而git rebase会将源分支上的提交逐个应用到目标分支上，形成一个线性的提交历史，看起来就像是在目标分支上单独进行开发一样。

分支结构：git merge会保留源分支和目标分支的独立分支结构，合并的结果形成一个新的合并提交。而git rebase将源分支上的提交逐个应用到目标分支上，导致源分支的提交被"移动"到目标分支上，使得提交历史更加线性简洁，但会改变分支结构。

合并冲突：当发生合并冲突时，git merge会在合并提交中保留冲突的标记，您需要手动解决冲突。而git rebase会在每个应用的提交上依次处理冲突，您需要在每个提交上解决冲突并继续rebase操作。

可读性：由于git rebase会将提交历史变得线性简洁，因此在查看提交历史时更容易理解每个提交的作用。而git merge则保留了源分支和目标分支的独立提交，可以更清楚地看到哪些提交来自源分支和目标分支。

选择使用git rebase还是git merge取决于您的需求和个人偏好。如果您希望保留分支结构并创建一个新的合并提交，可以使用git merge。如果您希望保持一个整洁的线性提交历史，并且不介意改变分支结构，可以使用git rebase。

## git cherry-pick

假设有两个分支：feature和master，并且你想要将feature分支上的一个提交应用到master分支上。以下是具体步骤：

首先，切换到master分支：git checkout master
运行git log命令查看要应用的提交的SHA值（例如：commit-A）。
执行git cherry-pick commit-A命令，将feature分支上的commit-A应用到master分支上。此时会创建一个新的提交，包含commit-A的更改。
如果存在多个提交需要应用，按照相同的步骤重复执行即可。

## git revert hash

取消某次提交记录，但是会生成一条git log