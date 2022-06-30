# Most frequently used Git Commands

## Configuration

+ **Username & Email**

  ```
  git config --global user.name "userName"
  git config --global user.email "emailAddress"
  ```

## Regular

+ **Initialize git**

  ```
  git init
  ```

+ **Status**

  ```
   git status
  ```

+ **Differeneces between previous & new code**

  ```
  git diff or git diff hashNo1 or git diff hashNo1 hashNo2
  ```

+ **Add in git**

  ```
  git add . or git add file-name or git add -A dir-name/
  ```

+ **Commit**

  ```
   git commit -m "msg"
  ```

+ **Link to repo**

  ```
   git remote add origin repo-link
  ```

+ **Push to repo**

  ```
  git push -u origin master
  ```

+ **Sync changed code**

  ```
  git pull origin master
  ```

+ **List of all changes**

  ```
   git log
  ```

  ```
   git log --stat
  ```

## Branch

+ New Branch:

  + **All branch**

    ```
     git branch
    ```
  
  + **All unmerged branch**

    ```
    git branch -a
    ```

  + **Create new branch**

    ```
     git branch branch-name
    ```

  + **Activate branch**

    ```
     git checkout branch-name
    ```

  + **Goto master branch**

    ```
    git checkout master
    ```

  + **Merge with master**

    ```
    git merge branch-name
    ```

  + **Check all branches merged with master**

    ```
    git branch --merged
    ```

  + **Push to repo**

    ```
    git push -u origin master
    ```
  
+ **Delete Branch** :

  ```
  git branch -d branch-name ( It'll delete locally )
  git push origin --delete branch-name

## History

+ **All previous commit**

  ```
   git log
  ```

+ **All previous commit with statistics**

  ```
  git log --stat
  ```

+ **Get which cmd has been made since beginning**

  ```
  git reflog
  ```

## Undo

+ Basic Undo :
  + **Undo the new changes ( It'll remove all the new changes in the particular file)**

    ```
    git checkout filename
    ```

  + **Change the recent commit message**

    ```
    git commit --amend -m "msg"
    ```

+ **Delete Commit from master & add that commit in particular branch**
  + 1st : coppy the particular hash(6-7 chars or full)
  + 2nd : goto desired branch

  ```
  git cherry-pick coppied-hash
  ```

  + 4th : goto master branch

  ```
  git reset --soft master-initial-commit-hash
  ```

## Clean

+ **Remove all untracked file & dir**

  ```
  git clean -df
  ```
