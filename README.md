# GIT Practice
### Q1 Create a Distributed version control system, and put files into it.
    1) Create a repository online
    2) git init -b main
    3) git add . 
    4) git commit -m "Initial Commit"
       Sets the new remote origin
    5) git remote add origin https://github.com/anshumankmr/Git-Practice
       Verifies the new remote URL
    6) git remote -v
       Pushes the changes in your local repository up to the remote repository you specified as the origin
    7) git push origin main

### Q2 Replicate a DVCS on your local machine, make changes to its files, and then put them back into it.
    1) git clone https://github.com/anshumankmr/Git-Practice   
    After making changes
    2) git add . && git commit -m "Formatting Fixes"
    3) git push origin main

### Q3 List down all the files which have changed in the last commit. List only the file names.
    Create a new file called temp.txt to observe the changes
    1) git diff --name-only HEAD HEAD~1
    $  README.md   
       temp.txt

### Q4 You’ve accidentally added some files on a DVCS. Remove those files from the DVCS without deleting them from your local system.
   The .gitignore file is a text file that tells Git which files or folders to ignore in a project.
   A local .gitignore file is usually placed in the root directory of a project. You can also create a global .gitignore file and any entries in that file will be ignored in all of your Git repositories.
   To create a local .gitignore file, create a text file and name it .gitignore (remember to include the . at the beginning). Then edit this file as needed. Each new line should list an additional file or folder that you want Git to ignore.
   To create a .gitignore file for the repository.
   >$ touch .gitignore
   Then in the gitignore file, we can add the name of the file we wish to ignore.

   In the case, we want to remove an already tracked file,
   Next you need to exclude the file from the repository. Probably you don't want to remove the file from your file system, this can be done with:
   >git rm --cached path/to/filename.extension

### Q5 You’ve accidentally committed some files on a DVCS. Revert the DVCS to a previous stable state
   git reset --hard commit_number

### Q6 Create a DVCS capable of supporting 2 similar dev environments. Make changes in the files which are present on both of them and then merge the environments into  one.

   Create a new file.
   > touch newfile.txt

   Create a new branch 

   > git branch newBranch 
   Switch to newBranch
   > git checkout newBranch
   
   Make some changes to the file.
   Commit the changes to newBranch.
   >git checkout main
   >git pull origin main
   >git merge newBranchs
   >git push origin main

### Q7 You have a DVCS supporting your prod, test and dev environments, you need to make sure that only a particular set of commits from the test environment are  added in the prod environment. What & how would you do it?

>git checkout -b add-log-component origin/add-log-component
git checkout master
git cherry-pick COMMIT-HASH-HERE
git push origin master

Git's cherry-pick command allows you to "cherry pick" only the commits you want from another branch.
Get back into the branch you're merging into. You'll likely do this by running git checkout master.
Find the commits you want to pull into your branch. 
"Cherry pick" the commits you want into this branch. Run this command: git cherry-pick hash-number. That will pull just this commit into your current branch.
Push up this branch like normal. git push origin master

## Scenario Questions:
### 1 If the central repository is two commits ahead of your local repository, how will you push your code ? 
    
   Commit the new changes to the current branch I am in.

    git add .
    git commit -m "Message"
    git branch newBranch
    git checkout newBranch
    git checkout main
    git pull origin
    git merge main
    git push origin newBranch

### 2 I have two branches, A and B, where A is my main branch, and B is a the branch with a new feature, describe the step by step process getting all of B’s code in A
   1) I commit the changes to the branch B using git add . && git commit -m "New Commit"
   2) I switch to the main branch using git checkout A
   3) I merge using git merge B.