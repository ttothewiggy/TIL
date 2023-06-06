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

Als