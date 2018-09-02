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
# get repo status
use "git status" to get the files' status.
# get diff 
use "git diff <filename>" to get the diffs with the former version.

