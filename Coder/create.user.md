## How to create first user in Coder

We incremently sussed out the process by starting small with

```
coder --help
```

This brought up the list of coder commands which we parsed thorugh to find the one we wanted. 
Which was: 

```
coder users
```

We used --help to find the next step:

```
coder users create
```

But we needed to login, and we then sussed that we create the first user as we login for the first time. 

```
coder login http://localhost:3000 --first-user-email 30057335@student.toiohomai.ac.nz --first-user-password coderpassword --first-user-username admin
```

Initially we ran it without the localhost 3000 name and port number and it produced this error:
build info: Get "https:///api/v2/buildinfo": http: no Host in request URLFailed to check server "https:" for first user, is the URL correct and is coder accessible from your browser? Error - has initial user: Get "https:///api/v2/users/first": http: no Host in request URL

It needed to be pointed to a port. 

When we added the localhost port it worked, and prompted us whether we wanted to start an enterprise 30 day trial which we responded 'No'. 
```
> Your Coder deployment hasn't been set up!
> Start a 30-day trial of Enterprise? (yes/no) no
                                                            
  Welcome to Coder, admin! You're authenticated.            
                                                            
  Get started by creating a template:  coder templates init 
```

View the Web UI: https://ganfhprtld4lq.pit-1.try.coder.app 

Followed the video here below but it's using a template that uses kubernetes, which I haven't set up so we started a template using the online GUI and docker and Stephen is currently trying to figure my recurring dpkg error. 

https://asciinema.org/a/htTWVG44oTuI4CI0tDOSs3UGb


Created new folder with copies of Docker tf template. Changed name in README

Added:  

    apache2 \
    tmux \

    below sudo \


BELOW IS THE CLI SESSION 
Here, we created a new folder in vscode and added 3 file to it, that were copies of the files in the docker template on coder.com.

build/Dockerfile
main.tf 
RAEDME.md

Below you can see we navigated to that folder called cs101. 

alexevans@Alexs-MacBook-Pro ~ % cd Documents/School/Placement/cs101 
alexevans@Alexs-MacBook-Pro cs101 % coder template create .
> Upload "."? (yes/no) yes
You are signed out or your session has expired. Please sign in again to continue.
Try logging in using 'coder login <url>'.                                        
alexevans@Alexs-MacBook-Pro cs101 % coder login http://localhost:3000
Your browser has been opened to visit:

	http://localhost:3000/cli-auth

> Paste your token here: 
> Welcome to Coder, admin! You're authenticated.
alexevans@Alexs-MacBook-Pro cs101 % coder template create .          
> Upload "."? (yes/no) yes
✔ Queued [366ms]
✔ Adding README.md... [-1ms]
✔ Setting up [6ms]
✔ Parsing template parameters [1ms]
✘ Cleaning Up [5ms]
run parse: recv parse source: load module:  ERROR: Invalid expression (main.tf:31)
> Expected the start of an expression, but found an invalid expression token.     
alexevans@Alexs-MacBook-Pro cs101 % coder template create .
> Upload "."? (yes/no) yes
✔ Queued [995ms]
✔ Adding README.md... [-1ms]
✔ Setting up [6ms]
✔ Parsing template parameters [7ms]
⧗  Detecting persistent resources 
  Terraform 1.3.4
  data.coder_workspace.me: Refreshing...
  data.coder_provisioner.me: Refreshing...
  data.coder_provisioner.me: Refresh complete after 0s [id=b9585451-7b09-465a-872a-7edaba56b8b9]
  data.coder_workspace.me: Refresh complete after 0s [id=b8254e31-f92a-44eb-8fdb-ba69d5a49b5f]
  coder_agent.main: Plan to create
  coder_app.code-server: Plan to create
  docker_volume.home_volume: Plan to create
  docker_image.main: Plan to create
  docker_container.workspace[0]: Plan to create
  Plan: 5 to add, 0 to change, 0 to destroy.
✔ Detecting persistent resources [8161ms]
⧗  Detecting ephemeral resources 
  Terraform 1.3.4
  data.coder_provisioner.me: Refreshing...
  data.coder_workspace.me: Refreshing...
  data.coder_workspace.me: Refresh complete after 0s [id=cf2603f7-0395-4f88-af95-45050aa5c20c]
  data.coder_provisioner.me: Refresh complete after 0s [id=05634949-8a9b-48d9-986c-3fe515e01406]
  coder_agent.main: Plan to create
  coder_app.code-server: Plan to create
  docker_volume.home_volume: Plan to create
  docker_image.main: Plan to create
  Plan: 4 to add, 0 to change, 0 to destroy.
✔ Detecting ephemeral resources [625ms]
✔ Cleaning Up [14ms]
┌────────────────────────────────┐
│ Template Preview               │
├────────────────────────────────┤
│ RESOURCE                       │
├────────────────────────────────┤
│ docker_container.workspace     │
│ └─ main (linux, arm64)         │
├────────────────────────────────┤
│ docker_image.main              │
├────────────────────────────────┤
│ docker_volume.home_volume      │
└────────────────────────────────┘
> Confirm create? (yes/no) yes
Validation failed.
alexevans@Alexs-MacBook-Pro cs101 % coder template create .
> Upload "."? (yes/no) yes
✔ Queued [547ms]
✔ Adding README.md... [-1ms]
✔ Setting up [5ms]
✔ Parsing template parameters [4ms]
⧗  Detecting persistent resources 
  Terraform 1.3.4
  data.coder_provisioner.me: Refreshing...
  data.coder_workspace.me: Refreshing...
  data.coder_provisioner.me: Refresh complete after 0s [id=605f75e5-b184-4be9-a9b6-1322e9ab4a24]
  data.coder_workspace.me: Refresh complete after 0s [id=30c5fea4-5f05-422b-a923-9f3232e5a017]
  coder_agent.main: Plan to create
  coder_app.code-server: Plan to create
  docker_volume.home_volume: Plan to create
  docker_image.main: Plan to create
  docker_container.workspace[0]: Plan to create
  Plan: 5 to add, 0 to change, 0 to destroy.
✔ Detecting persistent resources [6650ms]
⧗  Detecting ephemeral resources 
  Terraform 1.3.4
  data.coder_provisioner.me: Refreshing...
  data.coder_workspace.me: Refreshing...
  data.coder_provisioner.me: Refresh complete after 0s [id=b2094bdd-4a4f-426d-8bda-5040ad02d25a]
  data.coder_workspace.me: Refresh complete after 0s [id=f7f95914-1ac5-4c9a-9ef1-e95e0f099309]
  coder_agent.main: Plan to create
  coder_app.code-server: Plan to create
  docker_volume.home_volume: Plan to create
  docker_image.main: Plan to create
  Plan: 4 to add, 0 to change, 0 to destroy.
✔ Detecting ephemeral resources [623ms]
✔ Cleaning Up [16ms]
┌────────────────────────────────┐
│ Template Preview               │
├────────────────────────────────┤
│ RESOURCE                       │
├────────────────────────────────┤
│ docker_container.workspace     │
│ └─ main (linux, arm64)         │
├────────────────────────────────┤
│ docker_image.main              │
├────────────────────────────────┤
│ docker_volume.home_volume      │
└────────────────────────────────┘
> Confirm create? (yes/no) yes
Validation failed.
alexevans@Alexs-MacBook-Pro cs101 % 
alexevans@Alexs-MacBook-Pro cs101 % 
alexevans@Alexs-MacBook-Pro cs101 % 
alexevans@Alexs-MacBook-Pro cs101 % 
alexevans@Alexs-MacBook-Pro cs101 % 
alexevans@Alexs-MacBook-Pro cs101 % 
alexevans@Alexs-MacBook-Pro cs101 % 
alexevans@Alexs-MacBook-Pro cs101 % 
alexevans@Alexs-MacBook-Pro cs101 % 
alexevans@Alexs-MacBook-Pro cs101 % 
alexevans@Alexs-MacBook-Pro cs101 % cd ..
alexevans@Alexs-MacBook-Pro Placement % git clone https://github.com/coder/v2-templates.git
Cloning into 'v2-templates'...
remote: Enumerating objects: 1153, done.
remote: Total 1153 (delta 0), reused 0 (delta 0), pack-reused 1153
Receiving objects: 100% (1153/1153), 47.74 MiB | 10.34 MiB/s, done.
Resolving deltas: 100% (617/617), done.
alexevans@Alexs-MacBook-Pro Placement % cd v2-templates 
alexevans@Alexs-MacBook-Pro v2-templates % ls
README.md		docker-code-server	images			pod-with-docker
api.md			docker-in-docker	pod-gateway-ide		pod-with-eclipse
aws-linux-vm		docker-with-jupyter	pod-gateway-lang	pod-with-jupyter
aws-rdp-visual-studio	docker-with-vnc		pod-idea		pod-with-php
aws-spot		emoji-urls.md		pod-idea-vnc		pod-with-ruby
azure-linux		faq.md			pod-pycharm		pod-with-rust
changelog.md		gcp-rdp-visual-studio	pod-vs-code		pod-with-vnc
deprecated		gcp-ubuntu-docker	pod-with-code-server	videos.md
alexevans@Alexs-MacBook-Pro v2-templates % cd docker-code-server 
alexevans@Alexs-MacBook-Pro docker-code-server % ls
README.md	main.tf
alexevans@Alexs-MacBook-Pro docker-code-server % cat README.md                                      
---
name: Develop in a container in a Docker host with code-server
description: The goal is to enable code-server (VS Code Web) 
tags: [local, docker]
---

# code-server (VS Code) template for a workspace in a container on a Docker host

### Apps included
1. A web-based terminal
1. code-server IDE (VS Code Web)

### Additional bash scripting
1. Prompt user and clone/install a dotfiles repository (for personalization settings)
2. Prompt user for container image to use
3. Prompt user for repo to clone
4. Prompt user for which VS Code extension to install from the Open VSX marketplace
5. Clone repo
6. Download, install and start code-server (VS Code-in-a-browser)

### Authentication


### Resources
[NodeJS coder-react repo](https://github.com/mark-theshark/coder-react)

[Coder's GoLang v2 repo](https://github.com/coder/coder)

[Coder's code-server TypeScript repo](https://github.com/coder/code-server)

[Golang command line repo](https://github.com/sharkymark/commissions)

[Java Hello World repo](https://github.com/sharkymark/java_helloworld)

[Rust repo](https://github.com/sharkymark/rust-hw)

[Python repo](https://github.com/sharkymark/python_commissions)
alexevans@Alexs-MacBook-Pro docker-code-server %    