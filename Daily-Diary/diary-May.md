
# 03/05/23

So since the kids day event didn’t run, and that was the main deliverable for my project, and since there was no record of the one that was run in Amsterdam, it looks like I’m going to create a presentation for my project.Which is good, as I was worried I hand’t done enough coding for this project to get a pass. 
So I’ve been thinking about some sort of deliverable to show Bruce, I think setting up the container infant of him, or having it pre set up. Then tunnelling to it and running vscode with a website coded into a folder which when opened, has a game or a website or something. I could use Minecraft as well but I want something more relevant to school. But I might do both. Maybe get Bruce to load it up on his machine as well. 

So that’s the plan.
- Get vscode working in a container 
- Be able to access it remotely. - either coder or no vnc
- Add a folder to the container that’ll contain something interesting, like a game in a web browser you open with live server. And maybe Minecraft too. 
- Get Bruce to do it, so it needs to work on Windows.
- Maybe get whole class to do it. 

# 05/05/23

Today I went in to the iimaginarium and got help with a plan for the project. Stephen knew what to do and went about teaching me the foundations I needed to get cracking. 
The plan is to create a templete in coder using a terraform file and a dockerfile to pre load all the bits and create a workspace with everything I need to open a folder in vscode and edit it in the browser. 
It was a fiddely process, different to what I imagained and pretty much impossible for me to figure out on my own without some heavy guidance from Stephen and Abby. 
But by the end of the day we had a workspace up and running, using a template from the Coder github. (Reminder: Need to find the link to that repo). 

There was a lot of troubleshooting, see walkthrough-project.md file for detailed info. 

# 08/03/23

Today I tried to make some new templates and workspaces but I kept getting a validation error. Resolved that by dropping the full stop I was using in the coder template create command.
Now I’m just trying to clone a repo from github using the vscode terminal, which has worked. And now I’m just trying to open it with live server which isn’t working. I’m not sure how to proceed but I’m thinking that’ll be enough for the project if I can just get the group to follow the instructions on cloning a “lesson” and then opening it to code it.
I've also tried a couple other ways to get the lesson folder installed during the build, but the yaml option didn't work, git cloning in the dockerfile hasn't yet worked and I haven't tried the mkdir option yet but I'm going to give it a go tomorrow. 
Overall a successful day breaking things. 

