#Notes: Git Complete: The definitive, step-by-step guide to Git

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

git status -- check the status of the working directory files

git add [file-name]-- untracked files to be added to staging area before committing

git add . -- all untracked files are added / Used to recursively add the files (level1/level2/level3..)

git commit -m "commit message" -- comitting the files from the statging area

git commit -am "commit message" -- Adding and commit steps together with commit message

git pull origin main --[ITS IS EXTREMELY IMPORTANT TO DO A PULL BEFORE PUSH]-- to make sure you are aware of the changes made to the online repo.

git push origin main -- push commits to the remote repo. and the branch name mentioned

git ls-files -- list of all files git is tracking in the current folder

git reset file-name -- To move back to working directory state from the staging state

git checkout -- file-name -- To discard the changes in working directory


git init project-name  -- starting a new git project

git init -- adding git to an already existing project
 
rm -rf .git -- removes all the traces of git from a project/directory

rm -rf project-folder-name -- delete the project folder

fork -- will make the copy of the repository to my account

git clone https-url -- cloning the git repository to local 





