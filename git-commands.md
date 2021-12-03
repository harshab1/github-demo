# Notes: Git Complete: The definitive, step-by-step guide to Git

## Git installation:

git version (pre-installed on newer Mac OS versions)

## Global variables

git config --global -edit (Edit the global variables in form of text file)

git config --global user.name (set the global user name)

git config --global user.email (email address)

git config --global core.editor "mate -w" (text mate is added as default text editor)

## Stages:

Local: Working directory, Staging area, Local repository

Remote: GitHub, BitBucket etc

## Basic Git commands

git init project-name  --> starting a new git project

git init --> adding git to an already existing project
 
rm -rf .git --> removes all the traces of git from a project/directory

rm -rf project-folder-name --> delete the project folder

fork --> will make the copy of the repository to my account

git clone https-url --> cloning the git repository to local 

git status --> check the status of the working directory files

git add [file-name]--> untracked files to be added to staging area before committing

git add . --> all untracked files are added / Used to recursively add the files (level1/level2/level3..)

git commit -m "commit message" --> commiting the files from the statging area

git commit -am "commit message" --> Adding and commit steps together with commit message

git pull origin main -->[ITS IS EXTREMELY IMPORTANT TO DO A PULL BEFORE PUSH]-- to make sure you are aware of the changes made to the online repo.

git push origin main --> push commits to the remote repo. and the branch name mentioned

git ls-files --> list of all files git is tracking in the current folder

git restore --staged file-name or git reset file-name --> To move back to working directory state from the staging state

git restore file-name or git checkout -- file-name --> To discard the changes in working directory

## Moving and renaming files

git mv old-file-name new-file-name  -- renaming the file, git consider this as remane operation

mv old-file-name new-file-name -- git sees this bash operation as the old file being deleted and new file being added

git add -A -- recursively add anychanges happened in the repo. this will lead to git noticing the operation that occured is a rename one

## Deleting files

git rm file-name --> delete a file using git, it will be automatically staged 

rm file-name --> delete a file(tracked/untracked) using bash, had to be staged using add command (tracked only, obviously untracked will be gone)

rm -rf file-name --> recursive force deletion of a folder, needs to be staged and committed

git restore file-name  --> add the deleted files by bash back to working directory

git restore --staged file-name --> unsatge the files that are being deleted

## History:

git help log --> help of git log

git log --> all the commit logs with timestamp and commit messages

git log --abbrev-commit --> commit ID is shortend to few characters

git log --oneline --graph --decorate

git log id-range-start..id-range-end

git log --since="2 days ago"

git log -- file-name -- commits related to specific file

git log --follow -- file-name -- it will see the rename commit logs

git show commit-id -- diff changes made and detailed commit information

## Alias

git config --global alias.alias-name "some long command exclude the git from that command" 

Example: git config --global alias.hist "log --all --oneline --graph --decorate" 

git hist --> alias command for the long command above stored in ~/.config file

## Ignoring unwanted files / folders

create .gitignore file if didnt already exist and add file-name (file-name.extension)or pattern (*.extension) or a folder (folder-name/)

## Diff/merge tool

Download p4merge from perforce.com

configure the diff/merge:

git config --global mergetool.p4merge.path /Applications/p4merge.app/Contents/MacOS/p4merge

git config --global merge.tool p4merge

git config --global difftool.p4merge.path /Applications/p4merge.app/Contents/MacOS/p4merge

git config --global diff.tool p4merge

git config --global difftool.prompt false

git config --global mergetool.prompt false


git diff --> Difference between working directory and staging area

git difftool --> Visually see the above command using p4merge

git diff HEAD --> Differenc between last commit and staging area

git difftool HEAD --> Visually see the above command using p4merge

git difftool local-branch-name remote-repo/remote-branch-name --> Differnece between staging area and last commit

git difftool local-branch-name remote-repo/remote-branch-name --> Visually see the above command using p4merge

git diff -- file-name --> Changes happend in that specific file only

git diff commit-id-1 commit-id-2 --> Diff b/w commits, HEAD for last commit, HEAD^ for last commit minus 1










 














