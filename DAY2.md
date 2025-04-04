# Git Workflow: Staging and Pushing to Remote Repo

## Step 1: Git Workflow (Staging - Local Repo - Remote Repo)

The Git workflow typically involves staging changes in your local repository, committing those changes, and then pushing them to a remote repository like GitHub. Here's how it works:

### a. Stage Changes Locally

After editing your files locally, you need to add them to the staging area (i.e., Git tracks the changes):
```sh
# Add a specific file
git add <file-name>
# Add all files in the current directory
git add .
b. Commit Changes Locally
Once the changes are staged, commit them to the local repository with a meaningful message:

sh
Copy
Edit
git commit -m "Your commit message"
c. Push Changes to Remote Repository
After committing locally, push the changes to the remote repository (e.g., GitHub):

sh
Copy
Edit
git push origin <branch-name>
Step 2: Git Commands up to Git Push in Master
a. Initialize a Repository or Clone an Existing One
If you don’t have a local repository yet, initialize a new one or clone an existing remote repository:

sh
Copy
Edit
# Initialize a new Git repository
git init

# Clone a repository from GitHub
git clone <repository-url>
b. Check the Status of Your Repository
Before making any changes, it’s helpful to check the status of your repository:

sh
Copy
Edit
git status
c. Create and Switch to a New Branch (optional but recommended)
To work on a feature or bug fix, create a new branch and switch to it:

sh
Copy
Edit
git checkout -b new-feature-branch
d. Add Changes to the Staging Area
After editing or adding files, you need to stage those changes:

sh
Copy
Edit
# Add specific file
git add <file-name>
# Add all files
git add .
e. Commit the Staged Changes
Once you’ve staged the changes, commit them to your local repository:

sh
Copy
Edit
git commit -m "Added new feature or fixed a bug"
f. Push the Changes to the Master Branch on Remote Repo
Finally, push the committed changes to the master branch of the remote repository (e.g., GitHub):

sh
Copy
Edit
git push origin master
