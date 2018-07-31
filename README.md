# git-push-pull-document
Commands to push and pull project to git repository

# Create the new project in git server 
  ->gitub

# When you want to push new project from local to git server
  $ mkdir project_name
    Ex: $ mkdir test-project

# Copy project in above project folder
  $ mv test-project /home/user/test-project

## Add the project to local git 
   # This will use to add all the files to git 
      $ git add .
   # This will use to add particular/single file
      $ git add /home/user/test-project/text.txt 
      
# Commit the project changes
  $ git commit -m "Testing Comments message"
  
# git remote add 
  $ git remote add origin `link of the project`
   Ex :- $ git remote add origin https://github.com/GirishNA/Jasper-Soft-Report-Generation-using-Json.git
    
# Before push the code you need to pull the code
  $ git pull origin master
  
# push the code to git branch
  $ git push origin -u master
  
# To check the status of the code file
  $ git status
  
# To create new branch 
  $ git branch `branch-name`
    Ex :- $ git branch test
  
# To check the list of all branches 
  $ git branch 
  
# To Delete the branch from the list
  $ git branch -d `branch-name`
    Ex :- $ git branch -d test
    
# Force Fully Delete the branch 
  $ git branch -D <branch>
    Ex :- git branch -D test

# Rename the current branch to <branch>
  $ git branch -m <branch>
    Ex :- git branch -m text
  
# To get List all remote branches
  $ git branch -a
  
  
## To Ignore the some files when pushing to git repository

  $touch .gitignore
  $vim .gitignore
    Ex:- if you want to ignore the target folder and any .html files
    
        $ vim .gitignore
          target/
          *.html     
