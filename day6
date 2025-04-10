Topics :
======================

# git best practices
# git merging stretegy
# git clone 
# git rebase and merge 
# git cherry - pick
# git pull and git fetch 


# git best practices
===================================
  
1 Use clear commit messages.

2 Commit often but don’t commit everything.
  
3 Create feature branches.

4 Pull before pushing.

5 Avoid large merge commits.

6 Use .gitignore.

7 Prefer rebase to keep history clean.

8 Tag releases for easy reference.

9 Keep your history clean.

10 Collaborate using PRs for code review.

# Git clone command
==================================
  
  the git clone is uded to get a copy of code fro remote repo , make changes and push the the commits to the origin ( master ) if you have a accese to push on it  

           git clone < url >
  
  follow the steps :
______________________________________
  
  Step 1:  create a folder in Desktop
  Step 2: go inside that folder
  Step 3: Git clone <url>  -> Along with code, git config also will come
  Step 4: crate a staging branch, go there and start work .

NOTE: default alias name origin

git remote -v


Git Merging strategy
====================


1. Fast-Forward Merge:


Description: In a fast-forward merge, Git simply moves the pointer of the target branch forward to include the commits of the source branch. This happens when the target branch hasn't diverged since the source branch was created.
Scenario:
Assume we have a repository where master branch is the main branch and a feature branch was created from master. During the development on feature branch, no new commits were made to master.
Diagram:
Before Fast-Forward Merge:
mathematica
Copy code
      A --- B --- C  (master)
           \
            D --- E  (feature)
After Fast-Forward Merge (git merge feature):
mathematica
Copy code
      A --- B --- C --- D --- E  (master, feature)
Explanation:
Here, commits D and E from feature branch are simply added to the master branch in a linear fashion, as there were no new commits on master after branching off feature.




2. Recursive Merge (Three-Way Merge): [ORT merge strategy]


Description: Recursive merge (three-way merge) is used when changes have occurred on both the source (feature) and target (master) branches since they diverged. Git analyzes the changes and creates a new merge commit to reconcile the differences.
Scenario:
Suppose both master and feature branches have diverged with new commits.
Diagram:
Before Recursive Merge:
mathematica
Copy code
      A --- B --- C  (master)
           \
            D --- E  (feature)
After Recursive Merge (git merge feature):
mathematica
Copy code
      A --- B --- C --------- M  (master)
           \               /
            D --- E ------   (feature)

Explanation:
Git creates a new merge commit M that combines the changes from both branches (master and feature). Commits D and E are merged with master, preserving the history of both branches.




3. Merge and Rebase:
====================================

Description: While not strictly a merging technique, rebasing is an alternative approach to integrating changes from one branch (feature) into another (master). Rebase moves the entire branch onto a new base (typically the latest commit of master), rewriting the commit history.
Scenario:
Suppose you have a feature branch with several commits that you want to incorporate into master without creating a merge commit.

  Diagram :
  ____________________________
  
Before Rebase:
css
Copy code
      A --- B --- C  (master)
           \
            X --- Y --- Z  (feature)
After Rebase (git rebase master while on feature branch):
css
Copy code
      A --- B --- C --- X' --- Y' --- Z'  (master, feature)
Explanation:
Rebase moves the commits X, Y, and Z from feature branch on top of the latest commit (C) of master. This results in a linear history where the commits from feature branch (X', Y', Z') appear sequentially after C.





Git cherry-pick
==================
It will help us to merge only particular commits.

Git pull and git fetch
=======================

By using this commands , we will get an updated code from remote repo.



Git fetch
—---------
Git fetch —> local repo —> git merge —> working area
 
EX: git fetch origin test
     Git merge origin/test


Git pull
—--------
Git fetch + git merge.

EX: Git pull origin test


IQ: I want to change the recent commit message how?
ANS:
    git commit --amend -m "New commit message"
    git commit --amend —> editor will open
    git push --force —> push to remote to update the name
