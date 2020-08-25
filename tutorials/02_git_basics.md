# Git basics
## Get a git repository
 - Initialize a repository in an existing directory: ```git init```
 - Clone an existing repository: ```git clone <remote_url>```

![version control](images/27_lifecycle.png)<br>*The lifecycle of the status of your files*
## Record changes to the repository
 - Check files status: ```git status```
 - Track new files or stage modified files: ```git add <file_name>```
 - Track all files: ```git add .```
 - Unstage a file: ```git reset <file_name>```
 - Unstage all files: ```git reset```
 - Commit changes: ```git commit - m "commit message"```
 - Commit changes: ```git commit -m "text a log message"```
 - Skip staging area: ```git commit -a -m "text a log message"```
 - Remove unmodified files: ```git rm <file_name>```
 - Remove staging files: ```git rm -f <file_name>```. Be careful that the ```remove``` command will physically remove files in your disk.
 
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