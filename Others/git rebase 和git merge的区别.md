git rebase 和git merge的区别

rebase存在的价值是：对一个分支做“变基”操作，这意味着改变这个branch的初始commit。它会在新的base上一个一个地运行这个分支上的所有commits.这通常在当本地的工作(由一些列的commits组成）被认为是在一个过时的base基础上做的工作的时候才需要用它。还有一种场景，实际上并不是变基，而是为了清理你的分支上commits。

merge命令用法

git checkout feature

git merge master

feature分支中新的合并提交(merge commit)将两个分支的历史连在了一起，每次合并上游更改时feature分支都会引入一个外来的合并提交，这或多或少会污染你的分支历史，对开发者增加理解项目历史的难度。

rebase 命令用法

git checkout feature

git rebase master

git rebase - -continue 如果出现冲突，解决冲突后 git add 再执行continue，无需commit

git rebase - -abort 终止rebase行动，回到rebase之前状态

它会把整个feature分支移动到master分支的后面，有效地把所有master分支上新的提交并入过来。但是，rebase为原分支上每一个提交创建一个新的提交，重写了项目历史，并且不会带来合并提交。
