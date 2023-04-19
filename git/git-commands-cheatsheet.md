# Git Cheat Sheet

## Configuration

- `git config --global user.name "Your Name"`: Sets your username for Git.
- `git config --global user.email "your.email@example.com"`: Sets your email address for Git.
- `git config --global core.editor "nano"`: Sets your preferred text editor for Git.

## Repository Management

- `git init`: Initializes a new Git repository.
- `git clone <repository-url>`: Clones a Git repository from a remote source.
- `git add <file>`: Adds a file to the staging area for committing.
- `git add .`: Adds all changes to the staging area for committing.
- `git commit -m "Commit message"`: Commits changes to the repository with a descriptive message.
- `git push`: Pushes committed changes to a remote repository.
- `git pull`: Pulls changes from a remote repository into the local repository.

## Branch Management

- `git branch`: Lists all branches in the repository.
- `git branch <new-branch-name>`: Creates a new branch with the specified name.
- `git checkout <branch-name>`: Switches to the specified branch.
- `git merge <branch-name>`: Merges changes from the specified branch into the current branch.
- `git branch -d <branch-name>`: Deletes the specified branch.

## Viewing Changes

- `git status`: Shows the current status of the repository, including changes to files and the staging area.
- `git log`: Shows a history of commits made in the repository.
- `git diff`: Shows the differences between the working directory and the staging area.
- `git diff --staged`: Shows the differences between the staging area and the last commit.

## Undoing Changes

- `git reset`: Removes changes from the staging area.
- `git checkout -- <file>`: Discards changes made to a file in the working directory.
- `git revert <commit-hash>`: Reverts a specific commit by creating a new commit that undoes the changes.

## Miscellaneous

- `git remote -v`: Shows a list of remote repositories and their URLs.
- `git tag <tag-name>`: Creates a new tag for the current commit.
- `git fetch`: Downloads changes from a remote repository without merging them.
- `git stash`: Saves changes made to the working directory without committing them.
- `git clean -f`: Removes untracked files from the working directory.
