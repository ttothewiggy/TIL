
# Hosting a Website on Google Cloud 

I've began following a tutorial to host a website on google cloud. A friend of mine wants to have a basic website for his business, and I realised I could quite easily make a website for him but I have no idea how to host it or set it up. 
So I'm using this oppurtunity to figure it out. 

I'm following this tutorial: https://www.youtube.com/watch?v=f56PG7QxjFI&ab_channel=TonyTeachesTech

So far I've created an account with google cloud which as allowed me almost 500 dollars of free credit to play with.
I've created an instance of a VM and changed it to Ubuntu and modified the the settings to make it the cheapest possible/free. It'll only have 1GB of RAM and 30GB of space but that'll be fine for the needs of this website. 

Once the instance was up and running I connected to the server via SSH and ran some update commands
```
sudo apt-get update && sudo apt-get upgrade
```

The tutorial is using wordpress, and I want to use HTML, CSS and Javascript so I'm installing the web server Apache2 instead of what he's doing. 
I've asked chatGPT for help and I'm following the steps supplied by that as well as this tutorial now. 

```
sudo apt install apache2
```

I got the page up and running and got it to display a h1 heading saying "Hello" with web address just the IP I was allocated. So I'm in the process of linking the website domain name to that IP. 
But I've since found a more efficiant way to go about this that's a bit more suitable by using a Bucket to host a static website instead of having a VM. This website is going to be small and won't need the power a VM will provide. 
I am yet to get this working but I'm just waiting for the DNS propegation to come fully into effect. 