# git基本内容
git可以对项目进行远程拉取、本地提交、分支管理、版本控制等功能。给予项目开发的整体管理更好的体验。
# 基本命令
- git --version    查看git版本
- git config --global user.name "..."
- git config --global user.email "..."    设定用于提交到git的用户名和邮箱
- git init    创建初始化项目仓库
- git add  ...  将文件添加到暂存区
- git commit -m "..."    蒋暂存区内容提交到仓库中，可备注操作
- git push    将本地仓库内容推送到远程仓库
- git status    查看在上次提交后是否有对文件进行修改
- git diff    查看在上次提交之后对文件进行的改动，按q可以退出查看界面
- git log    查看历史提交记录，每次提交都有其唯一的id，按q可以退出查看界面
- git reset --hard ...     根据id回退到相应版本

例 git reset --hard HEAD^    回退到上个版本

- git reflog    可以查看所有分支的所有操作记录（包括已经被删除的 commit 记录和 reset 的操作），按q可以退出查看界面
- git ls-files    可以查看有哪些文件在暂存区中
- git checkout    当执行 git checkout . 或者 git checkout --  <file>命令时，会用暂存区全部或指定的文件替换工作区的文件（回复到上一次提交到暂存区的状态），若暂存区内没有相关文件（即文件还未提交过暂存区），则用版本库中的文件替换（回复到上一次版本提交的状态），当执行git checkout ...，可以将head指针切换到相应分支
- git restore    在2.23版本后新添加的命令，git restore <file>命令可以将文件回复到修改前的状态，git restore --staged <file>命令可以撤销暂存区的修改，将文件状态恢复到未 `add` 之前
- git remote    连接远程仓库
- git branch    可以查看本地分支，添加命令-r可以查看远程分支，-a可以查看所有分支，-d可以删除分支，git branch ...可以新建分支
- git merge    git merge ...合并相应分支
- git switch    在2.23版本后新添加的命令，为了避免git checkout用法的混淆，该命令用于切换分支 
