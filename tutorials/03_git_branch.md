# Git Branching
![version control](images/68_git_branch.png)<br>*Git branching. (98ca9, 34ac2, f30ab, c2b9e, 87ab2) are 
commits along the project history. (master and testing) are two branches originated from two commits 
(c2b9e and 87ab2) respectively. At this moment, the pointer (HEAD) is pointing to branch (master).*

## Branches in a nutshell
 - Create a new branch: ```git branch <branch_name>```
 - Switch branch: ```git checkout <branch_name>```
 - Shorthand to create and switch to a new branch: ```git checkout -b <branch_name>```
 - Create a branch at a tag: ```git checkout -b <branch_name> <tag>```
 - Delete a branch: ```git branch -d <branch_name>```
 
 
![version control](images/74_merge.png)<br>*Git merging.*
## Git merge
To merge branch (iss53) to (master), Git creates a new snapshot that combines (C4 and C5) and automatically
creates a new commit (C6) that points to it. In case there is a conflict, you have to manually fix and commit it.
To this end, branch master is pointed to (C6).  
 - Suppose (HEAD) is pointing to (master), the merge command: ```git merge <branch_name>```
 
## Branch management
 - Show branches: ```git branch```
 - Show branches and commits: ```git branch -v```
 
## Remote branches
 - Synchronize your work with a given remote: ```git fetch <remote>```
 - Push your data to a remote: ```git push <remote> <branch>```