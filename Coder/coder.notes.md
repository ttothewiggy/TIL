# Coder Notes

This is a file to hold tidbits of information that I thought were worth keeping track of. 

When using linux, I've had issues with all the docker images accumulating too much space in the storage of the OS. Keeping on top of it is paramount. 

This command has been useful in forcing all the current docker images to be removed. It's been good for when I've been spinning up loads of practice workspaces trying to get vscode to display my cloned repo in the build. 
Not so useful if you have other important images you don't want to delete. 
But it's been the only way to clear them as an error message appears saying "error response from daemon: conflict: unable to delete". 

```
docker rmi -f $(docker images -aq)
```

docker rmi: This is the command to remove one or more Docker images.
-f: It is an optional flag that stands for "force" and is used to forcefully remove the image(s) without prompting for confirmation.
$(docker images -aq): This is a command substitution enclosed within $(). It retrieves a list of all Docker image IDs using the docker images command and its options.
docker images: This command lists all the Docker images present on the local machine.
-a: This option shows all the images, including intermediate and dangling images (unused images).
-q: This option prints only the image IDs in a quiet mode (only outputs the IDs without any extra information).
So, when you run the complete command docker rmi -f $(docker images -aq), it will forcefully remove all the Docker images on your local machine without asking for confirmation.


