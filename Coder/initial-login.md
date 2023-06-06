
The easiest way to install Coder is to use our install script for Linux and macOS.

To install, run:

```
curl -fsSL https://coder.com/install.sh | sh
```

You can preview what occurs during the install process:

```
curl -fsSL https://coder.com/install.sh | sh -s -- --dry-run
```

You can modify the installation process by including flags. Run the help command for reference:

```
curl -fsSL https://coder.com/install.sh | sh -s -- --help
```

After installing, use the in-terminal instructions to start the Coder server manually via coder server or as a system package.

By default, the Coder server runs on http://127.0.0.1:3000 and uses a public tunnel for workspace connections.



To log into coder, use the CLI and input:
```
coder login coder.ii.nz
```
OR - To sign in on your own machine
```
coder login http://localhost:3000
```

That should open a coder window in the browser, with options to sign in with ither email or github, use github.
Paste the token produced into the CLI and go back to the browser and click open workspaces. 


You can change which port(s) Coder listens on.

```
# Listen on port 80
export CODER_HTTP_ADDRESS=0.0.0.0:80

# Enable TLS and listen on port 443)
export CODER_TLS_ENABLE=true
export CODER_TLS_ADDRESS=0.0.0.0:443

## Redirect from HTTP to HTTPS
export CODER_TLS_REDIRECT_HTTP=true

# Start the Coder server
coder server
```

Updade/Install coder with:

```
curl -L https://coder.com/install.sh | sh
```


# How to log in once you've already created first user




## Changes to the Coder Template

Stephen has edited the terraform file to help me in the right direction of creating an editable file on the desktop. 
To update a template you can use 
```
coder template push
```

Intead of deleting a workspace and template each time and rebuilding. 

#### In the Dockerfile

Added / tmux and /tree lines 7 + 8.
Tree is a nifty wee command the displays the folder structure in a more digestable way for beginner coders. 

#### In the Terraform file

Added at line 38 above the EOT:
```
mkdir website
    echo "<i>To update this page you will need to edit the <code>index.html</code> file in the home folder</i>" > ~/website/index.html
    echo "<i>To update this page you will need to edit the <code>/opt/cs101/index.html</code> file.</i>" > /opt/cs101/index.html
    python3 -m http.server --directory ~/website 8000 &
    python3 -m http.server --directory /opt/cs101 8001 &

```

This is echo a phrase in the port forward pthyon 3 8000 and 8001 options. 
As you edit the index.html file in vscode and save it, updates will be seen here. 

Now I'm going to try and add a repo from my github to pre load into the workspace. 