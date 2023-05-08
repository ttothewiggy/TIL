## This document will be a record of the steps taken to get school project 6214 working

The aim of the project is to run a workspace using Coder that'll open a desktop in the browser that contains an editable folder opened in VSCode that'll have a simple lesson to complete. 
It's to emulate what a lesson would look like using this technology.

### What we've done so far

I installed coder a while ago, you can follow the steps in the create.user.md file in this repo. 

Now, we've been throught the create new user process as I'm not using ii's login info this time. 


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

Initially we ran it without the "localhost 3000" name and port number and it produced this error:
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

To login with that user you point coder towards localhost
```
coder login http://localhost:3000
```

Then paste the token from the window. 

```
alexevans@Alexs-MBP ~ % coder login http://localhost:3000                 
Your browser has been opened to visit:

	http://localhost:3000/cli-auth

> Paste your token here: 
> Welcome to Coder, admin! You're authenticated.
```

### Next we created a template

I cloned a repo from coder for a simple docker template. 
Renamed it and saved it locally on my machine. 
I chanegd 2 things in the dockerfile build, adding apache2 \ tmux \ which are key to being able to edit the files in the container. 
```
apache2 \
tmux \
```


Using the cli, I used the one where we signed into coder, we create a template. 

```
coder templates create .
```
Respond to upload with yes. 
Confirm create yes. 

*** Been getting a lot of "Validation failed." errors. Trying to figure out why it worked the one time and not any other times. 

### Troubleshooting Validation error

So I've removed the added tmux and apache lines from the dockerfile to make it the exact same as the original template. 
And I've removed some whitespace at the bottom of the terraform file at line 144. Tf files are funny with whitespace. 
Fixed the error. Such a simple and annoying mistake, but all it was is removing the full stop at the end of coder templates create. 


### Creating a workspace

```
coder create --template="cs101" workspace name
```
y on confrim

