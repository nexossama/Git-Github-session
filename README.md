![Alt text](<images/datAi forms banner.png>)
**Brought to you by :DatAi Club 🤖**\
**Author: Ossama Outmani**

# Git-Github-session

## + Basic commands

### 1 - Create a Repository
### 2 - Clone a Repository
>git clone [repo-link]
### 3 - add files
- hello.txt
- hello2.txt
### 4 - add content to hello.txt
- hello.txt : hello from hello.txt

- hello2.txt : hello from hello2.txt
### 5 - check status
>git status

both files are untracked
### 6 - add hello.txt to staging area
### 7 - recheck status
>git status
- hello.txt is tracked
- hello2.txt is not tracked
### 8 - add everything to staging area
>git add .
### 9 - remove hello.txt from staging area 
>git rm --cached hello.txt
### 10 - recheck status
>git status
### 11 - re-add hello.txt
>git add hello.txt
### 12 - commit(save) all changes done till now
>git commit -m "adding hellos files"
### 13 - modify hello.txt
you can modify the existing content or 
add this line (or anything else)to the file :\
I am a new line 
### 14 - re-check status
>git status

you will find that hello.txt is again untacked , because of the new modification
### 15 - add and commit new changes
>git add .

>git commit -m "modifying hello.txt"
### 16 - let's check history of our all commits (modification)
>git log

detailed informations are given for each commit\
to get a more summurized history
>git log --oneline

## + Branching
### 1 - create a new branch
>git branch feature1
### 2 - switch to the feature1 branch
>git checkout feature1
### 3 - add file text.txt
### 4 - add content to text.txt
hello from feature1
### 5 - add and commit changes 
>git add .

>git commit -m "adding text.txt to feature1 branch"
### 6 - back to main branch
>git checkout main

you will notice that **text.txt** disappeared. This happens because it was created in another branch ,and since we did not merge yet feature1 branch onto main branch , this file is not detected when switching to main 

### 7 -add text2.txt after branching
+ you can add content to it
+ add to staging area
+ commit
### 7 - back to feature1 branch
> git checkout feature1

### 8 - modify content of text.txt
this time try to do it yourself : 
- modify content
- add modification to staging area
- commit changes with an appropriate commit message
### 9 - check history
> git log --oneline

all changes you made till now are listed except the last one made in main branch
### 10 - merge feature1 brach onto main branch
as you have seen before , everything we did in feature1 branch do not exist in main .So we need to do a merge 
- checkout to main branch  
>git checkout main
- proceed a merge 
>git merge feature1 

if a window opened , type a commit message and then close it , then commit will be performed automaticalli
### 11 - check history
(use the right command to do so)\
as you have see a new merge commit is created 

## + Revert

### 1 - checkout to main
### 2 - create text3.txt
- modify content
- add modification to staging area
- commit changes with an appropriate commit message
### 3 - check history
### 4 - choose commit to revert 
we will choose the "adding text2.txt" commit to revert
> git revert [commit id]

you will notice that text2.txt no longer exists, same for next commits
### 5 - check history
you will notice that a new commit is created

## + Reset
### 1 - checkout to main
### 2 - choose commit to revert 
we will choose the "adding text2.txt" commit to reset
> git reset [commit id]
### 3 - check history
you will notice that commits are actually deleted

## + Merge Conflicts
### 1 - go back to text.txt
+ change the first line to :\
hello from hello.txt main
+ add to staging area 
+ commit
### 2 - checkout to feature1 branch 
> git checkout feature1
+ change the first line to :\
hello from hello.txt feature1
+ add to staging area 
+ commit
### 3 - try merge feature1 onto main
> git checkout main

> git merge feature1

go back to the conflicting file (text.txt) and fix conflict by choosing correct lines to keep
### 4 - commit merge
### 5 - merge is done successfully

# Github
### 1 - push changes to the remote Reposetory
> git push
### 2- make a change in the github interface
change or add content to text.txt and commit directly from Github: \
added content to text.txt
### 3- pull new changes from remote
> git pull





