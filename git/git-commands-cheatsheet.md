## Setting up Git

git config --global user.name "Your Name": Set your username in Git.
git config --global user.email "your.email@example.com": Set your email address in Git.

## Creating and cloning repositories

git init: Create a new Git repository.
git clone <repository-url>: Clone an existing Git repository to your local machine.

## Making changes

git add <file>: Add a file to the staging area.
git add .: Add all changes to the staging area.
git commit -m "Commit message": Commit staged changes with a message.
git commit -a -m "Commit message": Commit all changes without staging.
git rm <file>: Remove a file from the working directory and staging area.
git mv <old-file-name> <new-file-name>: Rename a file.

## Branching and merging

git branch: List all branches in the repository.
git branch <branch-name>: Create a new branch.
git checkout <branch-name>: Switch to a branch.
git merge <branch-name>: Merge changes from a branch into the current branch.

## Reviewing changes

git status: Show the status of the working directory and staging area.
git diff: Show the difference between the working directory and the staging area.
git diff --cached: Show the difference between the staging area and the last commit.
git log: Show the commit history of the repository.

## Working with remotes

git remote: List all remotes in the repository.
git remote add <remote-name> <remote-url>: Add a new remote to the repository.
git push <remote-name> <branch-name>: Push changes to a remote branch.
git pull <remote-name> <branch-name>: Pull changes from a remote branch.

## Undoing changes

git reset <file>: Unstage a file from the staging area.
git reset --hard: Discard all changes since the last commit.
git revert <commit-hash>: Create a new commit that undoes the changes in a previous commit.
git checkout -- <file>: Discard changes to a file in the working directory.