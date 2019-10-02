# A03
Important Commands to Know
--------------------------------
+ $ git init -- initialize
+ $ git add -- add to repository
+ $ git status -- see unstaged and staged files
+ $ git reset -- remove files from staging area
+ $ git commit -m "commit message here" -- commit to branch
+ $ git add -A -- add everything to staging area
+ $ git log -- see commit just made
+ $ cd  -- change directory
+ $ cd .. -- previous directory
+ $ ls -- what's in directory
+ $ ls -la -- all info about directory
+ $ touch .gitignore -- ignore files (for files with sensitive info)

Install git
-------------------
**GIT**: A free and open-source version control system designed to projects of all sizes with speed

Follow the instructions (https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) to install git (if it's not already installed). Note that for this tutorial we will be using git on the command line only. While there are some great git GUIs (graphical user interfaces), I think it's easier to learn git using git-specific commands first and then to try out a git GUI once you're more comfortable with the command. 

Create a GitHub account
-------------------------------
**GITHUB**: Platform used by users to share and test code as well as it is provides hosting software development using GIT

Repository (Create/Track)
----------------------------
**Repository**: Location of where file are in
1. Create repository on GitHub
2. Configure your credentials: 
	* $ git config --global user.email "email@address.com"
	* $ git config --global user.name "Your Name"
4. Go to folder with desired projects: $ cd ./file_path/
5. Initialize git repository: $ git init
6. Link GitHub repository to local directory: 
	$ git remote add origin <repository URL>
7. Check if repository successfully linked:
	$ git remote -v
8. Add all files to staging area. Replace dot with filename to add specific files: 
	$ git add . 
9. Check staging area: $ git status
	To unstage a file: $ git rm --cached file_name 
10. Commit any changes to master branch: 
	$ git commit -m "COMMIT MESSAGE"
11. Push changes to master branch: $ git push origin master

Cloning
---------------------
**Clone**: Command on git that clone your branch on a local computer
	* $ git clone <repository URL> <WHERE U WANT TO CLONE>
	* e.g. $ git clone ../remote_repo.git .
		* $ git clone https://github.com/stval98/A03
2. List all repository information: $ git remote -v 
3. List all branches in repository (local and remote): $ git branch -a 
Commiting
----------------------
**Commit**: Command on git that selects branch


Push to (local/Remote)
-----------------------
**Push**: Command used on git that transfers commit commands from a local computer to a remote repo
**Pull**: Command used on git that downloads file from a remote repo and installs and update on a local computer
**Remote**: Command used on Git that creates a copy of a file on a local computer
1. Show changes made to files: $ git diff
2. Check staging area: $ git status
3. Add files to staging area: $ git add -A
4. Check changes made to staging area: $ git status
5. Commit changes to master branch: $ git commit -m "changes made"
4. Pull changes from master branch: $ git pull origin master
5. Push changes to master branch: $ git push origin master 

Merging Branches to Master and Deleting
--------------------------
**Branch**: Command on git that creates a branch
**Merge**: Command on git that merges two branches into one separate branch
**Creating a Local Branch:**
1. Create branch: $ git branch BRANCH_NAME
2. Switch to branch: $ git checkout BRANCH_NAME 
3. List local branches: $ git branch

**Delete a Local Branch:**
1. List branches merged in so far: $ git branch --merged
2. Delete branch locally: $ git branch -d BRANCH_NAME
3. List all branches: $ git branch -a
4. Delete remote branch: $ git push origin --delete BRANCH_NAME

Solve a Merge Conflict
----------------------
**Merge Conflict**: Command on git used when merge command has competing commits and needs users help to decide final merge
**Fetch**: Command on git that updates files from remote repository to local computer
1. Pull changes from master branch: $ git pull origin master
2. Check staging area to see file affected: $ git status
3. Inspect file to find conflict. Search for <<<<<<< HEAD conflict marker.
4. Make necessary changes to resolve the conflict. 
5. Commit changes: $ git commit -m "changes made"
6. Push changes to branch: $ git push

Links
-------------
https://rogerdudler.github.io/git-guide/
https://product.hubspot.com/blog/git-and-github-tutorial-for-beginners
https://www.freecodecamp.org/news/what-is-git-and-how-to-use-it-c341b049ae61/
http://guides.beanstalkapp.com/version-control/common-git-commands.html
