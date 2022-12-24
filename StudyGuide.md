what can git do?
-

Step to use:
- install git

*** get in the project folder:
- ADD, COMMIT, STAGE
+ git init
+ git status: to see which branch are we on and which file is untracked, what will be commited

+ git add <fileName or .>: add file to staging area
+ git checkout -- <fileName>: delete all the change compare to staging area (delete direct in the file)(ctrl Z to recover)
+ git reset HEAD <file>: unstage 


+ git commit -m "<comment>": pack all the files added with the comment
+ gitk: open gui windown 



- WORK WITH OLD VERSIONS:
+ git log: show old commit versions
+ git show <commitID>: show what that commit change the previous file
+ git diff: show different between current file(working directory) and the lastest commited(staging area) file. *But not show if there is a untracked file(new file)*

+ git reset -- soft  <commitID>: recovery the old commit and keep all the changes in staging area 
	    -- mixed <commitID>: recovery the old commit and keep all the changes in working directory
	    -- hard <commitID>:  recovery the old commit and delete all the changes (can recovery by ctrl z)

+ git reverse <commitID>: create a new commit that  deleted all what that commit change to the file 

- BRANCHING AND MERGING
+ git branch: show all branch exiting.
+ git checkout -b <branch>: create and switch to a new branch
+ git merge: merge branch (A<--B: git checkout A => git merge B)
+ git branch -D <branch>: delele branch



___________
IF YOU ARE FIRST TIME:
git config --global user.email "<accountgmail>"
git config --global user.name "<accountname>"
 




SOME DEFINITIONS:
- staging area: lastest commited file
- git repository: save all the change(commit)
SOMETHING EXTRA:

ls: list file/folder in folder
ls -a: list all
ls -al: list all in list format
ls <folder>: list in folder
