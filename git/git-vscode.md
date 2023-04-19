## How to use git and VSCODE

To get a newly created project from VS Code to GitHub, you can follow these steps:

1. Initialize Git in your project directory: Open your project in VS Code and open the terminal (Ctrl + ). Then run the command git init` to initialize Git in your project directory.

2. Create a new repository on GitHub: Go to GitHub and create a new repository with a name and description that match your project.

3. Add the remote repository: In your terminal, add the remote repository URL to your local repository with the command git remote add origin <remote repository URL>. Replace <remote repository URL> with the URL of your GitHub repository.

4. Commit your changes: Use the Git commands git add . to stage all changes and git commit -m "Initial commit" to commit the changes with a commit message.

5. Push to GitHub: Finally, push your changes to GitHub with the command git push -u origin master. This will push your local master branch to the remote repository.

Your project should now be on GitHub!