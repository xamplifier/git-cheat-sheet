# xAmplifier - Github Command Updated List
### How to Create a Repository [ Init , Clone ]

Create new local repository :
>> Initialize the local directory as a Git repository.

```sh
$ git init [project name]
```

Download from an existing repository :
```sh
$ git clone my_url
```
### How to remote a Repository [ Remote ]
Remote a repository : 
```sh
$ git remote add origin <url>
```
Show all remotes : 
```sh
$ git remote
```
View Info about the remote Repository : 
```sh
$ git remote -v
```
See remote Url : 
```sh
$ git remote show origin
```
Remove a remote : 
```sh
$ git remote rm origin
```

### How to Get Informations from your Repository [ Status, Diff , Blame , Show , Log ]

 See all the new or modified files that are not commited yet : 
```sh
$ git status
```
Show the changes to files that are not yet staged :
```sh
$ git diff
```
Show the changes to staged fles :
```sh
$ git diff --cached
```
Show all staged and instaged file changes :
```sh
$ git diff HEAD
```
Show the changes between two commit ids :
```sh
$ git diff commit1 commit2
```
See the change dates and author for a file :
```sh
$ git blame [file]
```
See all the file changes for a commit id and-or a file :
```sh
$ git show [commit]:[file]
```
Show all the change history { All the commits history} :
```sh
$ git log
```
Show the change history for a file or directory including diffs :
```sh
$ git log -p [file/directory]
```

### How to Work with Branches [ Branch , Checkout , Merge , Tag ]

List all locla branches :
```sh
$ git branch
```
List all branches, local and remote :
```sh
$ git branch -av
```
Create new Branch and call it new_branch :
```sh
$ git branch new_branch
```
Switch to a specific branch - {Switch to branch -> new_branch} :
```sh
$ git checkout branch
```
Create new branch and switch to it  : 
```sh
$ git checkout -b new_branch
```
Remove a branch called new_branch :
```sh
$ git branch -d new_branch
```
Merge branch1 into branch2 :
```sh
$ git checkout branch2
$ git merge branch1
```
Show any merged braches : 
```sh
$ git branch --merged .
```
Cancel a merge : 
```sh
$ git merge --abort .
```
Show remote branches : 
```sh
$ git branch -r
```
Show both local and remote branches : 
```sh
$ git branch -a
```
Rename branch : 
```sh
$ git branch -m oldName newName .
```
Tag a specific commit {i.e. new_tag commit} :
```sh
$ git tag new_tag
```
Tag a commit with a version : 
```sh
$ git tag -a v1.0.0 -m "Add Message"
```
Push tags into master remote : 
```sh
$ git push --tags
```

### How to make changes [  Add , Commit ]

Stage a file ,ready for commit : 
```sh
$ git add [file]
```
Staged all changes files ,ready for commit : 
```sh
$ git add .
```
or
```sh
$ git add *
```
Commit all your staged files and give a message to the commit : 
```sh
$ git commit -m "commit message"
```
Compose the above two commands in one {The 'add' and 'commit' commands} : 
```sh
$ git commit -am "commit message
```
Change last commit to repositoty tier (Only last one can change) : 
```sh
$ git commit --amend -m "message" file.txt
```
Revert a commit : 
```sh
$ git revert <commit>
```
### How to Unstage Files [ Checkout , Reset ]

Change a file back to history how they were at the last commit : 
```sh
$ git checkout --file.txt
```
Unstage file, keeping the file changes : 
```sh
$ git reset [file]
```
Change Repo but not Staging Tier : 
```sh
$ git reset --soft
```
Change Repo and Staging But not Working Tier : 
```sh
$ git reset --mixed
```
Change all three Tiers : 
```sh
$ git reset --hard
```
Change Repo to a specific commit :
```sh
$ git reset --hard [commitNo]
```
>>*If you reset or checkout a file don't push to a different branch.* Use ``` $ git push origin HEAD``` 
### How to Synchronize [ Fetch , Pull , Push ]

>Fetch before you work
>Fetch before you pull
>Fetch often

Get the latest changes from origin : 
```sh
$ git fetch
```
Get the latest changes from origin and merge also : 
```sh
$ git pull
```
Get the latest changes from origin and rebase : 
```sh
$ git pull --rebase
```
Push local changes to the origin : 
```sh
$ git push
```
Push and tells to the Git where to put our commits : 
```sh
$ git push -u origin <branch>
```
 > We use -u for the Git to remember the parameters so that next time we can simply run 'git push'
 
#### The Stash Command [ Stash ]
Stash : 
```sh
$ git stash save "text message"
```

Show what's in stash : 
```sh
$ git stash list
```

Bring back latest stash : 
```sh
$ git stash pop
```

Remove all stash : 
```sh
$ git stash clear
```
### Help Command

```sh
$ git command --help
```


### Git Hunks

Structure and Organise Commits before push : 
```sh
$ git add -p [FileName]
```

Stage this hunk [y,n,q,a,d,/,e,?]?
y=yes
n=no
q=quit


### General Info

View the Git Version : 
```sh
$ git version
```
View where the Git is located : 
```sh
$ which git
```
Remove untracked files from Working Tier : 
```sh
# Files
$ git clean -f 
# Directories
$ git clean -d  
```
Remove all the file with the same format : 
 ```sh
$ git rm '*.txt'
```
Rename or move a file : 
```sh
$ git mv [file]
```
