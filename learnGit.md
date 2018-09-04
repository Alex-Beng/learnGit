# init
usd "git init" command to init a file to a repository.
# add file
use "git add" command to add file(s) to a repository.
# commit file
use "git commit" to commit files to a repository.
with "-w" parameter can add notes.
AND!!! just like snapshot, each commit can be for version backward.
# view modifies
AND!!! so use the "git log" to see what each commit modify the file.
input 'q' to quit the logs.
# version rollback
use the "git reset " to rollback the version.
parameter "--hard <pointer>" to appoint the commit id(which can only write the former-four num) or HEAD^(can be written HEAD~<num>)
# find commit id
use the "git reflog" to get all the command history as well as each command's corresponding commit id.
# get repo status
use "git status" to get the files' status.
# get diff 
use "git diff <filename>" to get the diffs with the former version.
# 关联远程库
使用 "git remote add <远程库名> [仓库ssh/https 地址]" 将本地库与远程库关联
# 推送到远程库
使用 "git push" 是将当前分支推送到远程库.
第一次推送, "-u" 参数会将本地 master 分支与远程 master 分支关联, 并推送 master 分支的所有内容.
之后本地 commit 之后, 只要 "git push origin master".
# 创建&删除分支
使用 "git checkout <分支名>" 进行分支的创建,
"-b"  参数表示创建并切换.
"-d"  参数表示删除分支.
# 切换分支
使用 "git branch <分支名>" 切换.
使用 "git branch" 查看当前分支.
提交同上, 只不过是提交到了创建的分支上.
# 合并分支 
先切换到 其他 分支
使用 "git merge <分支名>" 将分支名对应分支合并到当前分支.
然后可以删除被合并分支
Just for conflict.