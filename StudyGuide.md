what can git do?
- manage project by controling commit vesions.
- github to work online and control source flow.

Step to use:
- install git

*** get in the project folder:
## ADD, COMMIT, STAGE
+ git init
+ git status: to see which branch are we on and which file is untracked, what will be commited

+ git add <fileName or .>: add file to staging area
+ git checkout -- <fileName>: delete all the change compare to staging area (delete direct in the file)(ctrl Z to recover)
+ git reset HEAD <file>: unstage 


+ git commit -m "<comment>": pack all the files added with the comment
+ gitk: open gui windown 



## WORK WITH OLD VERSIONS OF COMMIT:

+ git log: show old commit versions
+ git show <commitID>: show what that commit change the previous file
+ git diff: show different between current file(working directory) and the lastest commited(staging area) file. *But not show if there is a untracked file(new file)*

+ git reset -- soft  <commitID>: recovery the old commit and keep all the changes in staging area 
	    -- mixed <commitID>: recovery the old commit and keep all the changes in working directory
	    -- hard <commitID>:  recovery the old commit and delete all the changes (can recovery by ctrl z)

+ git reverse <commitID>: create a new commit that  deleted all what that commit change to the file 

## BRANCHING AND MERGING

+ **git branch**: show all branch exiting.
+ **git checkout -b <branch>**: create and switch to a new branch
+ **git merge: merge branch** (A<--B: git checkout A => git merge B)
+ git branch -D <branch>: delele branch

## GITHUB:

a place to store commit of the team

- git remote add origin <URL>: connect current local repo to the remote repo 
- git remote -v: display list of repo
- git push:  update the local repo to remote repo --- this will change the remote repo (remember to not push to master)
- git push -u origin <branch>: at the first time push local to remote
- git push origin <branch>: push change to a branch


- git clone <remoteRepo URL>: create a folder and copy the repo to computer
- git pull: aply all the change on remote repo to the exiting local repo(after cloned it)


**=> Step to create a pull request**
1. git checkout -b <subBranch>
2. git push origin <subBranch>
3. create a pull request
4. review code
   1. Review code online
   2. fetch branch into local to test offline
   3. appove pull request
5. merge to master

**CONFLICT**
1. When will a conflict happen?
   1. Changing the same file at the same row
   2. A delete file X, B modified file X
2. How to resolve a confict?
	# First method: using rebase
   1. In conflict branch: run 'git rebase master'
   2. Resolve conflict, 'git add' the edited file.
   3. Run 'git rebase --continue'
   4. Repush the branch to github: git push origin <branch> -f	
   5. Merge
	# Second method: merge
   1. https://www.youtube.com/watch?v=K4kzvzZ7v08&list=PLkY6Xj8Sg8-viFVtaVps_h_Emi2wQyE7q&index=17
   
   2. To lazy to study so watch that when necessary :>

___________
IF YOU ARE FIRST TIME:
git config --global user.email "<accountgmail>"
git config --global user.name "<accountname>"
 




## SOME DEFINITIONS:
- working directory: 
- staging area: lastest commited file
- git repository: save all the change(commit)
	+ local repo
	+ remote repo



## SOMETHING EXTRA:
+ls: list file/folder in folder
+ls -a: list all
+ls -al: list all in list format
 ls <folder>: list in folder



+ fork repo -> create a branch on your repo -> if u want to contribute to the main repo then create a pull request to it
+ to study README.md file: search 'MARKDOWN cheatsheet' and 'Markdown online editor"
+ issue tracking: report an issue
+ trending on github: show what is trending and we can vote a repo to make it trend
+ oh my zsh: custom terminal
+ GUI tools: 
+ search for Git GUI clients: sourve tree, git kranken, git desktop
+ 