# Git basics - Notes


[ToC]

## Credits :pray:
:::info
Credit goes to below content creators.
- CoreySchafer Git Fundamentals video  -  [CoreySchafer](https://www.youtube.com/watch?v=HVsySz-h9r4)
:::

## :point_right:Instantiation of Git 

### Check the git installation

:::success
**git --version**
:::

### Instantiate the Global variables

:::success
Set Username --> **git config --global user.name {username}**
Set Username --> **git config --global user.email {email}**
Retrieve the configured variables --> **git config --list**
:::

## :point_right:Git help

:::success
- **git help {action}**
- **git {action} --help**
:::

## :point_right:Initialize, revoke and check status of git in a folder
### Initialization

:::success
**git init**
:::


### Revoke

:::danger
**rm -rf .git**
:::

### Status

This command will share the information of all the tracked & untracked files and status of files.
:::info
==**git status**==
:::

## :point_right:Stage files to Stagging area - Local
### To stage a specific file

:::success
**git add {file_name}**
:::

### To stage ALL files

:::success
**git add -A**
:::

### To stage all files starting with data

:::success
**git add data***
:::

### To Ignore set of files from git tracking in folder

- Create a file with the name ==.gitignore==
- Add the file names or folder names to .gitignore.

### To reset particular file from staging.

This command will remove all the files form staging area

:::danger
**git reset {file_name}**
:::

### To reset all the files from staging.

This command will remove all the files form staging area

:::danger
**git reset**
:::


## :point_right:Commit the files to Git Folder - Locally

:::success
**git commit -m {descriptive_message}**
:::

## :point_right:Check the logs of previous commits

This command provides the information of previous commited 

- hash information
- Author information
- message of previous commit
- Date and time of commits

:::info
==**git log**==
:::

## :point_right:Git Clone
This command will create a copy of the repository to new directory for modifications. It can copy from local repo or from the remote repository 
### Git Clone from Directory

:::success
**git clone ../{from_directory.git} <to_directory>**
:::

==**.**== represents - Local directory and generally used for to_directory.
### Git Clone from remote with remote URL info

:::success
**git clone <github_url> <to_directory>**
:::
==**.**== represents - Local directory and generally used for to_directory.

## :point_right:View the branches for Repositories

### List all the local branches

:::info
**git branch -a**
:::
### List all the remote branches

:::info
**git branch -r**
:::

## :point_right:Adding branches

### Add a local branch for repository 

:::success
**git branch {branch_name}**
:::

### Add a remote branch tracking for local repository

:::success
**git remote add {git_remote_branch_name} {remote_branch_url}**
:::

## :point_right:Deleting branches
### Delete a local branch from repository

:::danger
**git branch -d {branch_name}**
**git branch --delete {branch_name}**
:::

### Delete a remote tracking branch for repository

:::danger
**git branch -d -r {branch_name}**
:::

### Delete a remote branch 
:::danger
**git push origin --delete {branch_name}**
:::


## Switch or checkout between branches

:::info
**git switch {branch_name}**
**git checkout {branch_name}**
:::

## :point_right: Workflow - Create local repo and attach to git remote repo

:::warning
```
# Creating a new file README.md
     echo "# flask-intro" >> README.md

# Initializing git
     git init

# Adding README.md to staging area
     git add README.md

# Commit the changes
     git commit -m "first commit"

# by default the name of the initial branch is MASTER
# below command will renamefrom "master" to "main"
     git branch -M main

# Add the origin of remote repository
     git remote add origin https://github.com/ruppalur/flask-intro.git

# push the changes to remote respository
     git push -u origin main
```
:::

## :point_right: Workflow - Existing local repo and attach to git remote repo
:::warning
```
# Add the origin of remote repository
     git remote add origin https://github.com/ruppalur/flask-intro.git

# by default the name of the initial branch is MASTER
# below command will renamefrom "master" to "main"
     git branch -M main

# push the changes to remote respository
     git push -u origin main
```
:::


## :point_right: Workflow - Merging a branch to Master
:::warning
```
# Switch to the Master branch 
    git checkout master
    
# Git pull all the changes down to master to makes sure Master repo is updated
    git pull origin master
    
# Check if the existing branch is merged to master
# Below command will display all the branches which are merged
    git branch --merged
    
# Merge the branch with master 
    git merge {branch_name}
    
# Push the repo to remote origin
    git push origin master
```
:::

## Disclaimer :thumbsup: 
:::info
This content is purely created for educational purpose for future referance and credits belongs to above acknowledged content creators  
:::