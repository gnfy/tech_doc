## git 将已有项目添加到仓库中
>     git init
>     git add *
>     git ci -am '初始化项目'
>     git push

## git命令简化

修改**~/.gitconfig**文件 
>     [alias]
>     st  = status
>     ci  = commit
>     co  = checkout
>     dt  = difftool
>     mt  = mergetool

修改完成后，命令简化如下： 
>     git status = git st

## git设置默认push
修改**~/.gitconfig**文件 
>     [push]
>     default = current

## git 查看远程仓库地址
>     git remote -v

## git 解决冲突的办法
> 自动合并
>
>     git stash
>     git pull
>     git stash pop

> 撤销本地修改
>
>     git reset --hard
>     git pull

> 手动合并代码
>
>      git dt filename // 其中 dt = difftool, 参考上面的 difftool

## git 代码回滚
> 本地代码库回滚-方法1
>
>     git reset --hard commit-id //回滚到指定的 commit-id 版本

> 本地代码库回滚-方法2
>
>     git co commit-id //回滚到指定的 commit-id 版本, co = checkout

> 仓库代码库回滚
>
>     git reset --hard commit-id //回滚到指定的 commit-id 版本
>     git push origin HEAD --force

## git 对比两个版本的修改
> 指定版本对比 
>
>     git diff commit-id-1 commit-id-2 filename // 其中 filename 没有的时候，则对比两次提交的所有代码

> 本地修改对比
>
>     git diff filename
