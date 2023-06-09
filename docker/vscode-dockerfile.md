
## How to build a dockerfile to run VSCode in a noVNC browser window

I wanted to take the progress made interning at ii, where we(they) have made a dockerfile that when built, will run a container with minecraft in it over a noVNC browser window, and make it more applicable to my school project. 
I thought getting VScode running on a browser would be a cool way to show how this could be used for educational purposes. 


1. I forked the repo found at this link. https://github.com/ConSol/docker-headless-vnc-container. 
Then clone the repo you just forked. This repo contains everything we need. 
To do this, I used the CLI to navigate to the folder where I wanted it, used mkdir vscode-container and ran `git clone https://github.com/ttothewiggy/docker-headless-vnc-container'

2. Once cloned, I opened it in VSCode and navigated to the "Dockerfile.debian-icewm-vnc" file and copied all of its contects into a new file I created called "Dockerfile", which was saved into the main folder "docker-headless-vnc-container". 

3. Next, I edited the file to suit my needs. 
Delete or comment out "USER 1000" on line 63 - This just adds restrictions to the user on the noVNC tunnel, not neccesary for now when testing. 
Below line 61 - Add the following code. 

- `RUN apt-get -y update && apt-get -y upgrade`
This command updates the list of available packages and upgrades the installed packages on the container.

- `RUN apt-get -y install wget gpg`
This command installs the wget and gpg packages, which are required to download and verify the Microsoft GPG key for VS Code.

- `RUN wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg`
This command downloads the Microsoft GPG key and saves it as a file named packages.microsoft.gpg in the current directory of the container.

- `RUN install -D -o root -g root -m 644 packages.microsoft.gpg /etc/apt/keyrings/packages.microsoft.gpg`
This command installs the packages.microsoft.gpg file as a trusted keyring in the /etc/apt/keyrings/ directory of the container.

- `RUN sh -c 'echo "deb [arch=amd64,arm64,armhf signed-by=/etc/apt/keyrings/packages.microsoft.gpg] https://packages.microsoft.com/repos/code stable main" > /etc/apt/sources.list.d/vscode.list'`
This command adds the VS Code package repository to the list of available sources in the container by creating a new file named vscode.list in the /etc/apt/sources.list.d/ directory and adding the required package repository information to it.

- `RUN rm -f packages.microsoft.gpg`
This command removes the packages.microsoft.gpg file from the container as it is no longer needed.

- `RUN apt install apt-transport-https`
This command installs the apt-transport-https package, which is required to securely download packages from the VS Code repository.

- `RUN apt update`
This command updates the list of available packages in the container.

- `RUN apt install code`
This command installs the VS Code editor inside the container using the package manager apt.

4. Next, navigate to src > common > scripts > vnc_startup.sh.
This script sets up the VNC password, starts the noVNC web client, and starts the VNC server. It also logs the connection options for the VNC and noVNC clients.

The script accepts several command-line options, which are explained in the help function of the script. Some of these options allow skipping the VNC startup procedure and executing the assigned command. Another option enables more detailed startup output.

The script also sets up the window manager, starts the code editor, and logs the connection options for the VNC and noVNC clients.

We're going to add `code --no-sandbox --user-data-dir` just below `$HOME/wm_startup.sh &> $STARTUPDIR/wm_startup.log` on line 109. 
This is going to open up VSCode automatically on start up. It's not a key feature but I thought it was handy. 

5. Save all the files and open up a CLI. I use Kitty. 
Navigate to the folder we're working in. `cd Documents/Scool/Placement/vscode-container/docker-headless-vnc-container` in my case. 
Make sure docker is running. `docker status`
Once in the folder run `docker build -t vscode .` - this will build the Dockerfile we've just edited. 

6. Once/if successfully built, run `docker run -p 6901:6901 vscode` - -p 6901:6901 maps port 6901 on the local machine to port 6901 inside the container. This allows you to access the VSCode environment through a web browser using the URL http://localhost:6901.

7. Open a browser and put in your own IP, in my case 192.168.11.24. Then add`:6901/?password=vncpassword` - This is the set password chosen in the file. 

`http://192.168.11.24:6901/?password=vncpassword`

This should have opened a desktop in your browser with VSCode running straight away! Awesome!