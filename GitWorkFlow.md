### These are the following steps to enable github on VSCode:

Credits: Cam Flowers: https://github.com/camunity

Git Workflow

### Setting up git: 

Step 1: Make a new project folder and start creating your files inside the folder.

Step 0: In a terminal window change into the project directory you want to start using with git

Step 1: Initialize a new git repository locally
       git init
               success: Initialized empty Git repository in /Users/cameronflowers/COMP/temp/python/OOP_Git/.git/

To check the status of your local repository:
       git status

Step 2: add modified files to git tracking history
       git add .

this is used to add everything in the folder

Step 3: commit your tracked history to your local repository
       git commit -m "some descriptive thing about what you're committing"
               success: 3 files changed, x insertions(+)
               test: git status
                       success: nothing to commit, working tree clean


and you're done! except everything is only local right now :(
Let's push it to Github!

### Adding your local repository code to Github (for the first time)
Step 1: Go to Github and add a new repository with the same name as your local project
       note: you should leave the default settings (don't check the add README box)

You should see a screen with some instructions for how to add code to Github
Copy the commands that look like the ones below:     

Step 2: Run these commands in your terminal in the directory with your project

   2A)
       git remote add origin https://github.com/yourusername/your_project_name.git
           success: you're on a new line
               test: git remote -v (command to list that your local git is connected to remotely... shows a list of your remote repos)
                       success:
                           origin  https://github.com/yourusername/your_project_name.git (fetch)
                           origin  https://github.com/yourusername/your_project_name.git (push)
   2B) 
       git push -u origin master(or branch name)
           success: Branch 'master' set up to track remote branch 'master' from 'origin'.

   Go back to Github and refresh and everything should be good!
   You've just pushed your local branch "master" to a new branch "master" on a remote Github repository called origin


### Adding Collaborators
   1. Go to your new Github repository on github.com and click Settings
   2. Under the manage access tab click invite a collaborator
   3. Add the github username or github email account of your teammates


### Pulling Code from Github as a Collaborator
   1. Go to the project repository your teammate started on Github
   2. Click the green code button and copy the link
   3. In your terminal navigate to the place you want to save the project folder
       run the command:
           git clone https://github.com/someUsername/your_project_name.git
       (replace the link with the one you copied!!)
   4. You should have a new folder with your_project_name in the directory you ran the last command in
   5. Change into the new folder
           cd your_project_name
   6. Open the folder in your text editor to start working on the files!


### Git workflow after everything has been initialized or after you've cloned: 

   (These are the steps you pretty much run over and over)

   Step 0: Before you start making new changes (SUPER SUPER SUPER IMPORTANT!)

           git pull

   This will pull any changes anyone's made to the remote repo so you are up to date!

   Once you have some new changes that you would like to save:
   To check the status of your local repository:
           git status

   Step 1: Add modified project files
           git add * -- used to add only the modified files in the folder


   Step 2: Commit all the modified project files
           git commit -m "some descriptive thing about what you're committing"

   Step 2.5: Git Status
           Check the name of the branch you're on. You can also see this at the bottom of your VSCode window

   Step 3: Push your local changes to some branch on Github
           git push -u origin branch_name

   Important note: replace branch_name with whatever branch you're on. This starts as master, but as you start working on new branches this will change!


### Working with new branches

   # To create a new branch called development:
           git checkout -b development

   (you can name your branch anything but normally we'll start off with: development)

   This command will switch you over to your new branch called development

   We use branches to start new commit histories to separate code features from one another as we work on them

   # To switch to any branch that's already created:
           git checkout branch_name

   (change branch_name to the name of the branch you want to checkout)


   # Pushing from new branch to Github
       Step 0: Make some changes on your new branch (make sure you're on the right branch!)

       Step 1: Add your modified changes
           git add *

       Step 1.5: Check git status
           git status

       Step 2: Commit your local changes
           git commit -m "some descriptive thing about what you're committing"

       Step 3: Push to your remote repository
           git push -u origin current_branch_name

   (change current_branch_name to whatever name is returned from git status or on the bottom of your VSCode window)

