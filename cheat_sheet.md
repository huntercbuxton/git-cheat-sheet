# creating a new repo

## create local repo in working dir
```script 
git init
``` 
# cloning a remote repo
 
## using ssh, github, and the key for 'Host *' in ssh config file:
```script 
git clone git@github.com:<github username>/ <github repo name>.git
```
### example: 
```script
$ git@github.com:huntercbuxton/git-cheat-sheet.git 
```

## using ssh, github, and the key from an ssh config file entry specifying User, Host, & HostName:
```script
git clone <host>:<github username>/<github repo name>.git
```
### example: 
```script
githubkey2:huntercbuxton/git-cheat-sheet.git
``` 
## using https and github
```script https://github.com/<github username>/<github repo name>.git
```

### example: 

```script
 https://github.com/huntercbuxton/git-cheat-sheet.git
```

# remote repos

## list remote repos
```script
 git remote -v
```
## add a remote repo
```script
 git remote add <new remote name> <new remote url>
```
## remove a remote repo

```script
 git remote rm <remote name>
```


# branches

## list remote branches
```script
 git branch -r
```
## list local branches
```script
 git branch
```
## list local AND remote branches
```script
 git branch -a
```
## switch to another branch
```script
 git checkout <branch name>
```
## create new branch (but stay on current branch)
```script
 git branch <new branch name>
```

## create new branch (AND switch to it immediately)
```script
 git checkout -b <new branch name>
```
## copy branch from local to remote repo
```script
 git push -u <remote name> <local branch name>
```

## delete local branch 
```script
 git branch -d <local-branch>
```
## copy branch from remote to local repo 
```script
 git fetch 
 git checkout <remote branch>
```
## copy new commits from one branch to another
```script
 git checkout <outdated branch>
 git merge <updated branch>
```

## output the current branch's tracking info 
```script
 git branch -vv
```


# commits 

## revise most recent commit with all uncommitted changes (don't do this if you have already pushed the most recent commit to the remote branch it tracks) 
```script
 git add -A
 git commit --amend
```


# tags 

## list tags
```script
 git tag
```

## push new tags to remote
```script
 git push --tags
```

## create a signed tag 
```script
 git tag -s <name> -m <message>
```

# managing file/dir revisions

## make git 'forget' a file (but don't delete it) (remember to add <file> to .gitignore first)

```script
 git rm --cached <file>
```

## delete a file (not just from git, but also from the filesystem)
```script
 git rm <file>
```

## discard ALL changes to ALL files since most recent commit 
```script
 git reset --hard HEAD
```

## view uncommitted changes for a specific file:
```script
 git diff <file name>
```



# misc commands

## view list of commits for current branch
```script
 git log
```

