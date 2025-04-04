# Git Workflow, GitHub Repository Setup, and Useful Git Commands for DevOps Engineers

## Step 1: Git Workflow 

In Git, **workflow** refers to the process of handling and organizing code changes. When working without branching, your workflow is simpler and typically follows these steps:

1. **Initialize Git**: Begin by creating a local Git repository to start tracking your project files.
   ```sh
   git init

Make Changes: You can start working on your files directly, modifying or adding new ones.

Stage Files: After making changes, you need to stage the modified files before committing. This tells Git to track the changes.
git add <file-name>      # Stage a specific file
git add .                # Stage all modified files

Commit Changes: After staging the files, commit them with a clear message about what was changed.
git commit -m "Commit message describing changes"

Push to Remote: After committing locally, push your changes to a remote repository (like GitHub) to share your work.
git push origin master    # Push to the remote repository (master branch)
Step 2: GitHub Repository Creation & Connection to Git
a. Create a Repository on GitHub
Go to GitHub and log in to your account.

Click the New button on the top left of the GitHub dashboard.

Name your repository and choose the visibility (either Public or Private).

Optionally, initialize the repository with a README file.

Click the Create repository button to create your new repository.

b. Connect Your Local Repository to GitHub
Once the GitHub repository is created, you need to link your local repository to it:

Navigate to your local project folder.

Initialize a Git repository if you haven’t already:

sh
Copy
Edit
git init
Add your GitHub repository as a remote:

sh
Copy
Edit
git remote add origin https://github.com/your-username/your-repository.git
Push your local repository to GitHub:

sh
Copy
Edit
git push -u origin master
