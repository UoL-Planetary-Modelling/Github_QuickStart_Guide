# Github_QuickStart_Guide: Basic info for how to get started working with Github
GitHub is a platform where you can store, share, and collaborate on software development projects. Here's a quick guide to help you get started:
 

 
## Creating a Repository:
- A GitHub repository (repo) is a centralized location where files and resources related to a project are stored and managed, serving as a collaborative platform for version control, code sharing, and project management.

- To create a new repository, click on the "+" sign in the upper-right corner of any page on GitHub, then select "New repository."
- Choose a name for your repository, add an optional description, and select if you want it to be public or private.
- Optionally, you can initialize the repository with a README file, which is a good practice for providing an overview of your project.

- To create a new repository, use the following commands in your terminal:

`git init              # Initialize a new Git repository in your project folder`

`git add .             # Add all files in the current directory to the staging area`

`git commit -m "Initial commit"   # Commit the changes with a descriptive message`
 
- After creating a repository, you can start adding files to it. To add files, navigate to your repository and click on the "Add file" button, then choose "Upload files" to upload files from your computer.


## Committing Changes:
- The purpose of a commit in a GitHub repository is to save and record changes made to files within the repository. When you commit changes, you are essentially creating a snapshot of the current state of the files at that moment in time. 
- Each commit typically represents a specific set of changes, such as adding new files, modifying existing files, or deleting files.

### Commits serve several purposes:
> - **Version Control:** Commits provide a history of changes made to the repository over time. This allows you to track the evolution of the project and revert back to previous states if needed.
> - **Collaboration:** Commits facilitate collaboration among team members by providing a way to share and review changes. Team members can see who made specific changes, when they were made, and what the changes were.
> - **Documentation:** Each commit is accompanied by a commit message, which should provide a concise description of the changes being made. These messages serve as documentation for the development process and help others understand the purpose and context of each change.
> - **Safety Net:** Commits act as a safety net by allowing you to save your progress frequently. If something goes wrong or if you make a mistake, you can easily revert back to a previous commit to restore a known working state.

- Once you've added some files or made changes to your repository, you can 'commit' them to your repository by providing a commit message that describes the changes you've made. Commit messages should be concise and descriptive to help others understand the purpose of the changes.

- To add files and commit changes to your repository, use the following commands:

`git add <file-name>   # Add specific files to the staging area`

`git commit -m "Commit message"   # Commit the changes with a descriptive message`


## Cloning:
- Cloning a repository is the process of making a copy of an existing repository from GitHub onto your local machine, allowing you to access and work with the repository's files and history locally.
- To clone a repository, navigate to the repository on GitHub, click on the "Code" button, and copy the URL provided. Then, use the git clone command in your terminal to clone the repository to your local machine:

`git clone <repository-URL>   # Clone the repository to your local machine`


## Forking:
- Forking a repository involves creating a personal copy of another user's repository on GitHub, enabling you to freely experiment with changes without affecting the original repository.
- You can fork a repository by clicking on the "Fork" button on the repository's page. This is useful for contributing to open-source projects or experimenting with someone else's code without affecting the original repository.
To fork a repository, simply click on the "Fork" button on the repository's page on GitHub.


## Setting up a Remote (online) Repository:
- To set up a remote repository on GitHub, first, create a new repository on the GitHub website following the steps mentioned earlier.
- Next, link your local repository to the remote repository by adding it as a 'remote' using the git remote add command. 

- After creating a new repository on GitHub, link your local repository to the remote repository using the following commands:

`git remote add origin <repository-URL>   # Add the remote repository as 'origin'`

`git branch -M main   # Rename the default branch (if needed). 'main' is typically the standard name used for a repo, but 'master' has been used historically which can sometimes cause issues with naming discrepancies`


## Pushing Changes:
- Git push is the command used to upload local repository changes to a remote repository, ensuring that any modifications made locally are reflected in the online version.
- Used when your local repository is ahead of the remote one.
- After making changes to files in your local repository, you can push those changes to your linked remote GitHub repository using the git push command. This uploads your changes to GitHub and updates the remote repository:

`git push -u origin main   # Push the local repository to the remote repository main`

`git push origin <branch-name>   # Push changes to the remote repository <branch-name>`



## Pulling Changes:
- Git pull is the command used to fetch and merge changes from a remote repository to the local repository, when the remote repository has been updated since your last synchronization. 
- This is used when the remote repository is ahead of your local one, and ensures your local copy remains synchronized with the latest changes made remotely.

- To sync your local repository with the remote repository on GitHub, use the git pull command to fetch changes from the remote repository and merge them into your local branch:

`git pull origin main   # Fetch changes from the remote repository and merge them into your local branch`


# Useful tips

## Downloading individual files

- You can download individual files from GitHub by navigating to the file and clicking the download button. This will save the file on your local machine. Note, this will not track the file.
- If you would like to download a file from a GitHub repo using the terminal, e.g. if you are in a remote ssh session, you can use wget. Locate the GitHub file you want in the browser, e.g. a jupyter notebook. Click on the "raw" button which will display the raw json format of the notebook, copy the url, and from your terminal execute wget \<copied-url\>, which will then download the file to your remote directory. Note this will not track the file.

