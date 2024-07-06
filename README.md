# Most frequently used Git Commands

# index

+ [Configuration](#configuration)
+ [Regular-cmd](#regular-cmd)
+ [Advanced-cmd](#advanced-cmd)
+ [Branch](#branch)
+ [History](#history)
+ [Undo](#undo)
+ [Clean](#clean)
+ [Tag](#tag)
+ [Seperate Brance and Merge](#seperate-branch)

# configuration

+ **Username & Email**

  ```
  git config --global user.name "userName"
  git config --global user.email "emailAddress"
  ```

# Regular-cmd

+ **init git**

  ```
  git init
  ```

+ **status**

  ```
   git status
  ```

+ **differeneces between previous & new code**

  ```
  git diff 
  or, 
  git diff hashNo1 
  or, 
  git diff hashNo1 hashNo2
  ```

+ **add in git**

  ```
  git add . or git add file-name or git add -A dir-name/
  ```

+ **delete file/dir**

    ```
    git rm fileName
    git rm -rf dirName\
    ```

+ **rename file/dir**

    ```
    git mv oldFileName NewFileName
    ```

+ **commit**

  ```
   git commit -m "msg"
  ```

+ **link to repo**

  ```
   git remote add origin repo-link
  ```

+ **push to repo**

  ```
  git push -u origin branchName
  ```

+ **sync changed code**

  ```
  git pull origin branchName
  ```

# advanced-cmd

+ **stash** : save uncommitted changes as draft.
  
  + init stash

    ```
    git stash
    ```
  
  + save stash with msg

    ```
    git stash save "msg"
    ```
  
  + show stash

    ```
    git stash show stash@{n}
    ```
  
  + stash branch

    ```
    git stash branch branchName
    ```
  
  + stash untracked file

    ```
    git stash -u
    ```
  
  + stash all file

    ```
    git stash -a
    ```
  
  + list of stash

    ```
    git stash list
    ```
  
  + aply stash

    ```
    git stash apply
    ```
  
  + push to master

    ```
    git push -u origin master
    ```
  
  + remove stash

    ```
    git stash drop
    git stash pop
    ```
  
  + remove last stash

    ```
    git stash pop
    ```

# branch

+ **New Branch**

  + **all branch**

    ```
     git branch
    ```
  
  + **all unmerged branch**

    ```
    git branch -a
    ```

  + **create new branch**

    ```
     git branch branch_name
    ```

  + **activate branch**

    ```
     git checkout branch_name
    ```
  
  + **compare branch**
  
    ```
      git diff branch1 branch2
    ```

  + **goto master branch**

    ```
    git checkout master
    ```

  + **merge with master**

    ```
    git merge branch-name
    ```

  + **check all branches merged with master**

    ```
    git branch --merged
    ```

  + **push to repo**

    ```
    git push -u origin master
    ```

+ **rename branch**

  ```
    git branch -m old_branch_name new_branch_name
  ```

+ **delete Branch** :

  ```
  git branch -d branch-name ( It'll delete locally )
  git push origin --delete branch-name

# history

+ **all previous commits of the branch**

  ```
   git log
   git log branchName
   git log fileName
   git log --oneline
   git log --oneline --graph --decorate
  ```

+ **history in timeframe**

  ```
  git log --since="2 months ago"
  ```

+ **full history of particular cmd**

  ```
  git show commitHashCode
  ```

+ **all previous commit with statistics**

  ```
  git log --stat
  ```

+ **get which cmd has been made since beginning**

  ```
  git reflog
  ```

# undo

+ Basic Undo :
  + **undo the new changes ( It'll remove all the new changes in the particular file)**

    ```
    git checkout filename
    ```

  + **change the recent commit message**

    ```
    git commit --amend -m "msg"
    ```

+ **delete Commit from master & add that commit in particular branch**
  + 1st : copy the particular hash(6-7 chars or full)
  + 2nd : goto desired branch

  ```
  git cherry-pick coppied-hash
  ```

  + 4th : goto master branch

  ```
  git reset --soft master-initial-commit-hash
  ```

+ **undo after added**

  ```
  git reset fileName
  ```

# clean

+ **remove all untracked file & dir**

  ```
  git clean -df
  ```

# tag

> Tag is always created after committing. Ex : release version.

+ create tag

  ```
  git tag -a tagName
  ```

+ tag list

  ```
  git tag --list
  ```

+ show tag

  ```
  git show tagName
  ```

+ difference between tag

  ```
  git diff tagName1 tagName2
  ```

+ tag a particular commit

  ```
  git tag -a tagName commitCode
  ```

+ update tag particular commitCode

  ```
  git tag -a tagName -f commitCode
  ```

+ delete tag

  ```
  git tag --delete tagName
  ```

# seperate-branch

+ create seperate branch
  ```sh
  git checkout --orphan new-branch
  git rm -rf .
  ```

+ merge
  ```sh
  git checkout dev
  git merge orphan_branch_name --allow-unrelated-histories --no-ff -m "Merge orphan branch into dev"
  ```