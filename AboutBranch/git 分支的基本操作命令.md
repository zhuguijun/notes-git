git 分支的基本操作命令

git branch  查看本地分支名

git branch -a  查看所有的分支名

git branch -r 查看所有的远程分支

git checkout 分支名 切换分支

git checkout -b 分支名  新建本地分支

git checkout -b 本地分支名x origin/远程分支名y   拉取远程分支y并创建本地分支x，并自动切换到本地分支x

git fetch origin 远程分支y：本地分支x     拉取远程分支y并创建本地分支x，但不会自动切换到该新建分支，需手动checkout

git branch -d 分支名  删除本地分支

git branch -D 分支名  强制删除本地分支

git push - - delete origin 远程分支名  删除远程分支

git branch -m （分支名） （重命名分支名） 重命名本地分支

git push origin 本地分支名：远程分支名  推送代码到远程分支

git branch - -set-upstream dev origin/dev  将本地分支与远程服务器分支相关联

git push -f origin dev (远程分支名） 强制推送本地分支代码，覆盖远程仓库分支代码

git merge dev 将dev分支合并到当前分支

git rebase dev 将dev分支合并到当前分支

