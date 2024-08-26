# Project Name

Islam Hakeem Repo


## Usage

brief about Version control 


--------------------------------------------------
# why we use git ?

1- Track evrything in project
2- History track 
3- save everything changed 
4- evrychange have a uniq Id 
------------------------------------------------------

1- In first this is concept of VCS 

![Concept Image](concept.svg)

# git have 3 States of a Git Project 

Working tree -- stageing area -- repoitory 

![Three States](areas.png)

## 1- working tree : 
is the directory on your local machine where you are currently working on files. It contains the actual files and directories that you see and edit.
evrything you Added(file - -folder - image - anything)in your projects , in this case called untracked file 
and state => untracked assign to letter (U)

to go next step use (git add . to make all changed in staging area) or ( git add <fileName>) 

## 2-staging area :
 staging area second step after W.T in this case state of files (Modified) and ready to push to your repo , after commited ,
every commit have a unique ID called (hash - SHA_1) that is save your changed hitory if need back  to it .

The staging area is an intermediate area where changes to files are gathered before they are committed. It’s like a preview of the next commit. When you stage files, you're telling Git, "I want to include these changes in the next commit."
assign to letter (M)

## 3-The repository
 is where Git stores all the information about the project, including the history of all the commits, branches, tags, and more. The repository contains the actual commits, which are snapshots of the project at various points in time.

### there are Remot and local Repository :

local Repo -> in your machine not showing to anyone 
Remote Repo -> version of your project that is hosted on the internet or another network. It allows multiple developers to work on the same project from different locations. GitHub, GitLab, and Bitbucket are popular platforms that host remote repositories.
git host [bitbucket -- gitlab -- github]


# Git basics :

## Initializing a Repository : 

go to your directory and open terminal then use this command  "$ git init" This creates a new subdirectory named .git that contains all of your necessary repository files

if you want start your repo , create a file "file1.txt" and use
$ git add file1.txt
$ git commit -m "Initial commit"

## Cloning an Existing Repository
to clone a existrepo on any host "git clone <url>"


## lifecycle of the status of your files
![lifecycle of state file](lifecycle.png)
Checking the Status of Your Files "$git status" show you all changes status

## see what you’ve changed 
not yet staged type git diff with no other arguments to see changes in W.T
staged type git diff --staged  This command compares your staged changes to your last commit

## Viewing the Commit History
When you run "$git log" in this project, you should get output
1- commit hash (SHA-1) 
2- commit messege
3- date
4-auther 
"$git log --oneline -10" see last 10 commits only 


## Undoing Things
### $ git commit --amend

use this command if you need to edit commit messege

### git checkout -- README.md

This command discards any local changes you have made to the README.md file and reverts it to the last committed version in your local repository.
If README.md is modified in your working directory and you haven't staged the changes yet, this command will reset the file back to its state in the last commit.

### git reset
1. Unstaging Files (git reset HEAD <file>):
If you've staged files using git add but haven't committed them yet, you can unstage them with:  git reset HEAD <file>
This command removes README.md from the staging area, but keeps your changes in the working directory.

2. Soft Reset (git reset --soft <commit>):
Keeps your changes in the staging area (index) and working directory but moves the HEAD pointer to the specified commit.
git reset --soft HEAD~1

3. Mixed Reset (git reset --mixed <commit>):
Unstages the changes (removes them from the index) but keeps the changes in your working directory.
git reset --mixed HEAD~1

4. Hard Reset (git reset --hard <commit>):
Removes the changes from the staging area and working directory, resetting everything to the specified commit. This is destructive and cannot be undone.
git reset --hard HEAD~1

### git restore and argument with it

 git restore is a command used to restore files in your working directory to a specific state. It can be used with several arguments depending on what you want to restore:


1. git restore <file>: This will discard changes in the working directory for the specified file, reverting it to the state of the last commit.
Restoring Changes from the Staging Area:

2. git restore --staged <file>: This will unstage changes that have been added to the staging area but leave them in the working directory.
Restoring to a Specific Commit:

3. git restore --source <commit> <file>: This restores the file to its state in the specified commit, whether it's a commit hash or a branch name.

## Working with remote
1. Adding Remote Repositories :: $ git remote add <Url>
2. if you have more remote you can show it by :: $ git remote -v
3. to get all branches in remote host :: $ git fetch
4. get all changes in remote :: $ git pull


## Tagged 

tag is a reference to a specific point in the commit history. Tags are often used to mark important points in the repository's history, such as releases or milestones. There are two main types of tags in Git:

1. create Tag : git tag -a v1.0 -m "Version 1.0 release" creates an annotated tag named v1.0 with a message.
2. Viewing Tags : git tag
3. To view details of a specific tag, especially annotated tags, use: git show <tagname>
4. Pushing Tags : git push origin <tagname>
5. Deleting Tags : git tag -d <tagname>
















