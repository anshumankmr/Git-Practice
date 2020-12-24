# GIT Practice
## Q1 Create a Distributed version control system, and put files into it.
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

## Q2 Replicate a DVCS on your local machine, make changes to its files, and then put them back into it.
    1) git clone https://github.com/anshumankmr/Git-Practice   
    After making changes
    2) git add . && git commit -m "Formatting Fixes"
    3) git push origin master

## Q3 List down all the files which have changed in the last commit. List only the file names.
    Create a new file called temp.txt to observe the changes
    1) git diff --name-only HEAD HEAD~1
    $  README.md   
       temp.txt

## Q4 You’ve accidentally added some files on a DVCS. Remove those files from the DVCS without deleting them from your local system.
   The .gitignore file is a text file that tells Git which files or folders to ignore in a project.
   A local .gitignore file is usually placed in the root directory of a project. You can also create a global .gitignore file and any entries in that file will be ignored in all of your Git repositories.
   To create a local .gitignore file, create a text file and name it .gitignore (remember to include the . at the beginning). Then edit this file as needed. Each new line should list an additional file or folder that you want Git to ignore.
   To create a .gitignore file for the repository.
   >$ touch .gitignore
   Then in the gitignore file, we can add the name of the file we wish to ignore.
