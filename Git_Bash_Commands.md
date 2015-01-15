# Important GitBash commands 
## Creating and managing files and directories
pwd 
* print working directory
clear   
* clears the screen
ls 
* lists files and folders in current working directory
cd 
* changes the directory
* without any argument takes you back to your home directory
* cd .. allows you to change directory one level above your current directory
* cd filepath takes you to that directory which becomes your working directory
mkdir
* makes a new directory
* makdir directory_NAME
touch
* creates a new file
* touch filename
cp
* stands for copy
* cp file_name_you_want_to_copy directory_to_which_you_want_to_copy_to_in_your_working_directory
* cp -r argument_1 argument_2  (copies all the files from the directory in argument_1 to the files in argument_2) 
rm
* stands for remove
* rm file_to_remove
* rm -r directory_name  (removes all the files in that directory but there is not undo so be very careful!)
mv
* stands for move
* mv file_name_you_want_to_move directory_to_which_you_want_to_move_to_in_your_working_directory 
* can also use mv to rename files)
* mv old_file_name new_file_name
echo
* will print whatever arguments you provide
* echo Hello World!	
date
* prints out the date
* date
		
## Editing user name and email
* git config --global user.name "Type in your Username"
* git config --global user.email "Type in your E-mail"
* git config --list  	(shows all your details)

## Greating repos in your home directory
* mkdir ~/test--repo   	(create directory)
* cd ~/test--repo
* git init				(Initialize a local Git Repository in this directory)	
* git remote add origin https://github.com/MarnusOlivier/repo_name.git	(point your local repository at the remote repository you just created on the GitHub server)

## Adding, committing, pushing, branches, update and merging  
### Adding
This adds the changes you made to the index stage.
Suppose you add new files to a local repository under version control.
You need to let Git know that they need to be tracked.
* git add filename
* git add .		(adds all new files)
* git add -u	(updates tracking for files that changed names or were deleted)
* git add -A	(does both of the previous)

### Committing 
This adds the changes you made to the head stage, the final stage on the working repository.
You have changes you want to commit to be saved as an intermediate version.
* git commit -m "message"  	(where message is a useful description of what you did)
							(this only updates your local repo, not the remote repo on Github)

### Pushing 
The changes are now in the HEAD of the local working copy. To send those changes to your remote repository they need to be pushed.
For some reason i do not understand yet you first have tot do the following prior to pushing your file onto Github.
* git pull origin master

You have saved local commits you would like to update on the remote (Github)
* git push
* git push master

###Branches 
Branches are used to develop features isolated from each other. The master branch is the "default" branch when you create a repository. Use other branches for development and merge them back to the master branch upon completion.
Sometimes you are working on a project with a version being used by many people.
You want to edit that version.

You can then create a branch with the command:
* git checkout -b branchname

To delete a branch you can do the following:
* git branch -d branchname

To see what branch you are on type:
* git branch

To switch back to the master brach type:
* git checkout master

A branch is not available to others unless you push the branch to your remote repository:
* git push origin brachname

### Update and merge
To update your local repository to the newest commit, execute:
* git pull
in your working directory to fetch and merge remote changes.

To merge another branch into your active branch (e.g. master), use
* git merge branchname
In both cases git tries to auto-merge changes. 
Unfortunately, this is not always possible and results in conflicts. 
You are responsible to merge those conflicts manually by editing the files shown by git. 
After changing, you need to mark them as merged with:
* git add filename
Before merging changes, you can also preview them by using:
* git diff source_branch target_branch

## Cloning
Copying a repo to your local machine:
* git clone url_you_would_like_to_clone




