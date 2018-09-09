# init
```
usd "git init" command to init a file to a repository.
```
# add file
```
use "git add" command to add file(s) to a repository.
```
# commit file
```
use "git commit" to commit files to a repository.
with "-w" parameter can add notes.
AND!!! just like snapshot, each commit can be for version backward.
```
# view modifies
```
AND!!! so use the "git log" to see what each commit modify the file.
input 'q' to quit the logs.
```
# version rollback
```
use the "git reset " to rollback the version.
parameter "--hard <pointer>" to appoint the commit id(which can only write the former-four num) or HEAD^(can be written HEAD~<num>)
```
# find commit id
```
use the "git reflog" to get all the command history as well as each command's corresponding commit id.
```
# get repo status
```
use "git status" to get the files' status.
```
# get diff 
```
use "git diff <filename>" to get the diffs with the former version.
```
# 关联远程库
```
使用 "git remote add <远程库名> [仓库ssh/https 地址]" 将本地库与远程库关联
```
# 推送到远程库
```
使用 "git push" 是将当前分支推送到远程库.
第一次推送, "-u" 参数会将本地 master 分支与远程 master 分支关联, 并推送 master 分支的所有内容.
之后本地 commit 之后, 只要 "git push origin master".
```
# 创建&删除分支
```
使用 "git checkout <分支名>" 进行分支的创建,
"-b"  参数表示创建并切换.
"-d"  参数表示删除分支.
"-D"  参数删除未合并的分支.
```
# 切换分支
```
使用 "git branch <分支名>" 切换.
使用 "git branch" 查看当前分支.
提交同上, 只不过是提交到了创建的分支上.
```
# 合并分支 
```
先切换到 其他 分支
使用 "git merge <分支名>" 将分支名对应分支合并到当前分支.
然后可以删除被合并分支
但是默认使用是 Fast Forward 模式, 在删除分支之后会丢失分支信息
"--no-ff" 参数强制禁用 Fast Forward 模式, 并会提交一个新的 commit 以保留分支信息.
```
# 冲突管理
```
在不同分支进行修改后, 再进行合并可能会出现 conflict, 这时候需要手动修改再提交.
```
# 储藏现场( 用于bug分支 )
```
在 dev 进行开发的分支, 若要 fix bug, 需要保存当前进度, 修复后继续开发.
使用 "git stash" "储藏"起来.
然后 checkout 到需要修复 bug 的分支, 然后创建一个临时分支.
修改后与原分支合并, 删除临时分支.
然后返回开发分支继续开发.
使用 "git stash apply" 恢复现场, 但是这样 stash 的内容并不删除.
使用 "git stash drop" 来删除 stash 的内容.
使用 "git stash pop" 相当于以上两个一起执行.
```
# 强制删除未合并分支
```
参见删除分支的 "-D" 参数.
```
