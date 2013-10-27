# Welcome to the Augustana Web Guild

## Developer information

### Install software
1. Download and install [xampp](http://www.apachefriends.org/en/xampp.html)
1. Download and install [git](http://git-scm.com/downloads)

### Create an account on Github
1. Go to github.com and sign up
1. Click account settings > SSH Keys *(Follow the instructions in need help you might have run ``` mkdir ./ssh ``` before ``` cd ./ssh ```)*
1. Email guild@augustana.edu with your github username and request to be added to the developers team

### Create an account on pivotal tracker
1. Sign up on the [pivotal tracker website](https://www.pivotaltracker.com/)
1. Email guild@augustana.edu and request to be added to Development Projects

### Checking out code
1. Clone this project to your desktop *(run comands in git bash)*

    ```
    git clone git@github.com:awguild/WebGuild.git ~/desktop/WebGuild
    sh ~/desktop/WebGuild/scripts/Windowscheckout.sh //type yes if prompted for rsa fingerprint
    ```

### Doing an update
  1. Make sure Apache is running in XAMPP
  1. Open the project's folder in a text editor (like Sublime)
  1. Open the git bash 

    ```
    cd /c/xampp/htdocs/<projectName>
    ```
  1. Pull newest changes 
    
    ```
    git pull origin
    ```
  1. Create a new branch

    ```
    git checkout -b [Name]
    ```
  1. Edits files to satisfy user story
  1. Stage changes and commit
   
    ```
    git add .
    git commit -m "[description of what you did in this commit]"
    ```
  1. Push your feature branch to github

    ```
    git push -u origin [Name]
    ```
  1. Create a pull request (use [fixes #*storyID* in the commit message)
  1. Merge pull request (if applicable wait for someone to review your work)
  1. Delete your feature branch from github (click the *delete branch* button)
  1. Clean up your local repo 

    ```
    git checkout master
    git pull origin master
    git branch -d [feature branch name]
    ```
  1. Copy files from htdocs to folder on freya (until we have post commit hooks set up)

## Administrative Tasks

###Creating new repo
  1. Sign in to github and change your context to awguild
  1. Click the *New repository* button (Set the repo name to match the folder name in freya; set to public; ignore README;)
  1. Click *Create Repository*
  1. Copy code from freya to the desktop
  1. In GitBash, do 

    ```
    cd ~/Desktop/<NameOfProject> //changes directory to project directory
    git init //initializes a new git repo
    git add . //stages all the files for the next commit
    git commit -m "Initial commit" //creates a commit with the message "Initial commit"
    git remote add origin <SSH URL> //creates a new remote called origin that points to this project's Github SSH URL
    git push -u origin master //pushes the master branch to your origin remote (GitHub)
    ```
  1. Check repo on GitHub to make sure you have all the files
  1. Add repo to checkout script(s), should look like
   ```
   git clone git@github.com:awguild/<projectName>.git /C/xampp/htdocs/<projectName>
   ```
  1. Log into pivotal tracker as guild@augustana.edu
  1. Grab the api token from AugustanaWebGuild > Profile
  1. Click the Settings > Service Hooks on the github repo (not account settings, the repo settings)
  1. Paste the api token, check the active box, and hit update
