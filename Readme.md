## Install software
1. Download and install [xampp](http://www.apachefriends.org/en/xampp.html)
1. Download and install [git](http://git-scm.com/downloads)

##Creating Github account
1. Go to github.com
1. Create an account
1. Click account settings
1. SSH Keys (Follow the instructions in need help you might have run ``` mkdir ./ssh ``` before ``` cd ./ssh ```)
1. Email guild@augustana.edu with a text file that has your ssh public key (admin will add your key to all relevant projects)

##Creating new repo

1. Go to GitHub.com and sign in as awguild (guild@augustana.edu/webguild159753)
1. Click “New repository” button
1. Name it to match the folder name in freya; set to public; ignore README; Create Repository
1. Copy code from Freya to the desktop
1. In GitBash, do 
```
cd ~/Desktop/<NameOfProject> //to change directory to your desktop
git init //initializes repository
```
1. Go into GIT GUI and Open Existing Repository, then browse to repo and open
1. Rescan, Stage Changed[sic], add Commit Message of "initial commit," and then Commit
1. Go back to GitBash and add Github SSH as your remote origin:
```
git remote add origin <get SSH url from Github setup and paste here>
git push -u origin master //Tells it to push master branch to origin (GitHub)
```
1. Check repo on GitHub to make sure you have all the files
1. Add repo to checkout script (it makes sense, I swear!)

## Doing an update
1. Open the folder in a text editor
1. Open the git bash 
```
cd /c/xampp/htdocs/<projectName>
```
1. Pull newest changes git pull origin
1. Create a new branch
```
git checkout -b [Name]
```
1. Make edits to files
1. In the Git GUI Rescan, stage changes, commit
1. In the bash 
```
git push -u origin [Name]
```
1. Create a pull request (use [fixes #*storyID* in the commit message)
1. Merge pull request
1. Delete branch on server
1. In bash 
```
git checkout master
git pull origin master
git branch -d [Name]
```