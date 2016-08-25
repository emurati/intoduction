Ernel Murati
August 19, 2016
Introduction


================================ BASIC GIT COMMANDS ================================

$ git			- Check if git runs on the machine
$ git init		- To make a directory of your repository
$ git status		- Check the status of the repository, working and staging area
$ git add		- Add a file into the stain area before saving the changes
$ git add -p <file>	- Add some changes in <file> to the next commit
$ git reset HEAD <file>	- Un-stage a file from the stain area to the working area
$ git commit —m	 “…”	- Commit to a project and adding comments
$ git commit -am “…”	- Adds file to the stain area and commits them (shortcut)
$ git commit —-amend	- Change the last commit
$ git rm <file>		- Remove a file from the working area (needs commit)

$ git add <file> 
$ git rm <new_name>	- When renaming, we delete and then add the same file with new name
$ git mv <file> <file>	- Moving a file to a folder, moving a file to a file is renaming

$ git log		- Keeps a log of the changes, author, date and note of commit
$ git log -p <file>	- Show the changes over time for a specific <file>
$ git blame <file>	- Show the author of the changes to a the <file>
$ git diff		- Compares changes between repository and working area
$ git diff —-staged 	- Compares changes between repository and staging area
$ git diff —-cashed	- Gives the changes made to the files in the stain area

$ git checkout <num> —- <file>	- Go to the commit and copy that file to the working area


================================ BASIC GITHUB COMMANDS =============================

$ git remote add <repo> <URL>	- To match the repository key with a nickname
$ git remote		- List the number of Github repositories present
$ git push -u <repo> master	- Push the local repo to Github

$ git branch		- Shows the branches available
$ git branch <branch>	- Creates a branch to the master
$ git checkout <branch>	- Get on the branch
$ git branch -D <branch>	- Deletes a branch
$ git merge <branch>	- It merges the branch in command with the master
$ git push <repo> <branch>	- Pushes branch to repo


======================================== UBER =======================================

= Create a repository for Team or Personal
$ git remote add origin gitolite@code.uber.internal:TEAM/mycoolrepo	
$ git remote add origin gitolite@code.uber.internal:personal/${USER}/mycoolrepo

= Push to master (add a README to be safe)
$ git push -u origin master

= To clone a repo
$ git config --global -l	- Check  that you have url.ssh.. for code.uber.internal
$ git clone code.uber.internal:<repository>

$ git checkout -b branchname	- To create and branch out in one step EM_feature

= Rebasing
$ git checkout develop
$ git pull origin develop
$ git checkout your_branch
$ git rebase develop
$ git push origin +your_branch

= Bisecting
$ git checkout master
$ git pull
$ git bisect start
$ git bisect bad
$ git bisect good <last good commit hash>
$ git bisect run fab test:uber.tests.failing.test
