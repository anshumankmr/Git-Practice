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
    1) git clone https://github.com/anshumankmr/Git-Practice   
    After making changes
    2) git add . && git commit -m "Formatting Fixes"
    3) git push origin master