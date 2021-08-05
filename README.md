# My Most Used Git Commands

## Regular :
+ Initialize git : git init
+ Status : git status
+ Differeneces between previous & new code : git diff or git diff hashNo1 or git diff hashNo1 hashNo2
+ Add in git : git add . or git add file-name or git add -A dir-name/
+ Commit : git commit -m "msg"
+ Link to repo : git remote add origin repo-link 
+ Push to repo : git push -u origin master 
+ Sync changed code: git pull origin master

## Branch :
+ New Branch:

  + All branch : git branch
  + Create new branch : git branch branch-name
  + Activate branch : git checkout branch-name
  + Goto master branch : git checkout master
  + Merge with master : git merge branch-name
  + Check all branches merged with master : git branch --merged
  + Push to repo : git push -u origin master 
  
+ Delete Branch :
  
  + 1st : git branch -d branch-name ( It'll delete locally )
  + 2nd : git push origin --delete branch-name

## History :
+ All previous commit : git log
+ All previous commit with statistics : git log --stat
+ Get which cmd has been made since beginning : git reflog

## Undo : 
+ Basic Undo :
  + Undo the new changes : git checkout filename ( It'll remove all the new changes I made in the particular file)
  + Change the recent commit message : git commit --amend -m "msg" 

+ Delete Commit from master & add that commit in particular branch :
  + 1st : coppy the particular hash(6-7 chars or full)
  + 2nd : goto desired branch
  + 3rd : git cherry-pick coppied-hash
  + 4th : goto master branch
  + 5th : git reset --soft master-initial-commit-hash

## Clean : 
+ Remove all untracked file & dir : git clean -df
