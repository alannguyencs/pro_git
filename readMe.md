This tutorial:
- summarizes <b>[Pro Git](https://git-scm.com/book/en/v2)</b> written by Scott Chacon and Ben Straub.
- summarizes Git lecture provided by IBM on Coursera.

 # Config
  - Show config: `git config --list --show-origin`
  - Update identity: 
    ```sh
    git config --global user.name alannguyencs
    git config --global user.email alannguyen.cs@gmail.com    
    ```
  - Two ways to configuring Git to store/cache the password:
     - store: `git config --global credential.helper store`
     - cache: `git config --global credential.helper cache`
  - Help: `git help`
  
# Git basics
## Get a git repository
 - Initialize a repository in an existing directory: ```git init```
 - Clone an existing repository: ```git clone <remote_url>```

## Record changes to the repository
 - Check files status: ```git status```
 - Track new files or stage modified files: ```git add <file_name>```
 - Track all files: ```git add .```
 - Unstage a file: ```git reset <file_name>```
 - Unstage all files: ```git reset```
 - Commit changes: ```git commit - m "commit message"```
 - Skip staging area: ```git commit -a -m "text a log message"```
 - Remove unmodified files: ```git rm <file_name>```
 - Remove staging files: ```git rm -f <file_name>```. **Be careful** that the ```remove``` command will physically remove files in your disk. Do not be confused between removing files and unstaging files.
 
## View the commit history
 - Show all: ```git log```
 - Show k recent commits: ```git log -k```
 
## Working with remotes
 - Show the name of your remotes: ```git remote```
 - Show the name + url of your remotes: ```git remote -v```
 - Add a remote repository: ```git remote add <remote_name> <remote_url>```
 - Fetch data from a remote repository: ```git fetch <remote_name>```
 - Push committed data to a remote server: ```git push <remote_name> <branch>```
 - Rename a remote: ```git remote rename <current_remote_name> <new_remote_name>```
 - Remove a remote: ```git remote remove <remote_name>```
 
## Tag
Like most VCSs, Git has the ability to tag specific points in a repository's history as being important.
 - List your tags: ```git tag```
 - Create a tag: ```git tag -a v1.4 -m "tag message"```
 - Update tag to a new commit: ```git tag -fa v1.4 -m "tag message"```
 
 # Git Branching
## Branches in a nutshell
 - Create a new branch: ```git branch <branch>```
 - Switch branch: ```git checkout <branch>```
 - Shorthand to create and switch to a new branch: ```git checkout -b <branch>```
 - Create a branch at a tag: ```git checkout -b <branch> <tag>```
 - Create a branch at a commit: ```git checkout -b <branch> <commit>```
 - Delete a branch: ```git branch -d <branch>```


## Branches merging
To merge branch (iss53) to (master), Git creates a new snapshot that combines (C4 and C5) and automatically
creates a new commit (C6) that points to it. In case there is a conflict, you have to manually fix and commit it.
To this end, branch master is pointed to (C6).  
 - Suppose (HEAD) is pointing to (master), the merge command: ```git merge <branch>```
 
## Branch management
 - Show branches: ```git branch```
 - Show branches and commits: ```git branch -v```
 - List all tracking files in a branch: ```git ls-tree -r <branch> --name-only```
 
## Remote branches
 - Synchronize your work with a given remote: ```git fetch <remote>```
 - Synchronize + Merge: ```git pull <remote>```
 - Push your data to a remote: ```git push <remote> <branch>```
 - Delete a remote branch: ```git push <remote> --delete <branch>```
