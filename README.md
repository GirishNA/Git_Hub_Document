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
          
 ### To ADD Contribuiters/members in git
      goto -> settings -> collaborators -> psw :- ******  -> search the members based on git id and -> Add collaborators
      
### How to ADD GIT Version Control In Intelij IDE Tool
      goto -> file -> settings -> version Control -> git hub -> select password -> enter :- login and password -> Test -> Apply -> Ok
      goto -> inteliJ left down -> version control -> log 
     

### To Solve `remote: Invalid username or password` this issue in Windows pls do this Process
    ## You may have to check windows credential manager and delete the github entry under
     control panel -> user accounts -> credential manager -> Windows credentials -> Generic credentials

    ## After this Run These commands
      git config --global --unset user.name
      git config --global --unset user.email


### Refresh the Remote branch into local 
	git remote update origin --prune


### Uploading Large size files
	
	Note :- If you get these types of issues/warnings follow the bellow steps 
		`warning: LF will be replaced by CRLF in EMR/MyNewWork/.idea/workspace.xml.`	

## To get started with Git LFS, the following commands can be used.

		 1. Setup Git LFS on your system. You only have to do this once per
		    repository per machine:

		        git lfs install

		 2. Choose the type of files you want to track, for examples all XML
		    FILES / IMAGES, with git lfs track:

		        git lfs track "*.xml"

		 3. The above stores this information in gitattributes(5) files, so
		    that file need to be added to the repository:

		        git add .gitattributes

		 3. Commit, push and work with the files normally:

		        git add file.xml / git add . 
		        git commit -m "Add disk image"
		        git push

### If We are getting Filename too long Error 
		ex :- error:open("EMR/MyNewWork/common_model/Enterprise-Data-Platform/
			SourceCode/DataWareHouse_Updated/spark/entertainment/src/main/
			scala/com/emaar/entertainment/DataIngestion/NavisionIngestionCDCLoadClient.scala")
			:Filename too long
			 error: unable to index file EMR/MyNewWork/common_model/Enterprise-Data-Platform/SourceCode/
			DataWareHouse_Updated/spark/entertainment/src/main/scala/com/emaar/entertainment/DataIngestion/NavisionIngestionCDCLoadClient.scala
			fatal: adding files failed 

## Use Bellow cmd 
		$ git config core.longpaths true

### If you get `git another process running ` issue Then run the below cmd 
	
		issue ex :- Another git process seems to be running in this repository, e.g. an editor opened by 'git commit'. Please make sure all processes are terminated then try again. If it still fails, a git process
			    may have crashed in this repository earlier: remove the file manually to continue.


## Use Bellow cmd
		$ rm -rf .git/index.lock

