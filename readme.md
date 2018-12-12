# Working directory
- Area where all of our files and directories and changes are living all the time

# Staging Area
- Files and Directories that are explicitly add to the staging area

# Git Repository
- Where all our snapshots are stored


# Commands [STAGING AREA]
- Git Basics
    git init - initialize a git repository .git (a hidden directory)
    git status
    git add filename - add files that needs to be tracked
    git commit -m "Message here - always in present tense verb"

- Git Checkout
    git log - see the timeline and reference to the number of commits
    

- Adding multiple files of certain type
    git add *.html

- Adding all files in directory (including hidden)
    git add -A 
        adds all files and folders from the directory that you are in.
        useful to add everything in your project all at one time
    -----------------------------------------------
    Creating a hidden file in cmd
    -----------------------------------------------
    Files starting with a dot are by default hidden. You can create it simply by
        touch .httName
    anyone will still be able to see it using
       ls -a
    If you want files to be properly hidden, you will have to change folder permissions using chmod. For example
       chmod 770 folder_name
    will prevent users (except the owner and people in the group) from listing the whole directory "folder_name".

- Removing files ( after adding using git add )
    git reset HEAD filename 

- Ignoring files
    https://help.github.com/articles/ignoring-files/
    
    If you create a file in your repository named .gitignore, 
    Git uses it to determine which files and directories to ignore, 
    before you make a commit.
    
    If you already have a file checked in, and you want to ignore it, Git will not ignore the file if you add a rule later. 
    In those cases, you must untrack the file first, by running the following command in your terminal:
        git rm --cached FILENAME
    