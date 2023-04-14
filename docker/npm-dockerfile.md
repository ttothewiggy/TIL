We added a Dockerfile to an old react project to see if we could containerise it. 

```
FROM node:alpine3.17
# Chose alpine to run the dockerfile beacuse it was the best match for node. It brings all the base stuff pre installed. 


COPY React/ /usr/react
# This line copies the contents of the React directory on the host machine to /usr/react inside the Docker image. The second line is commented out and appears to be an alternative way of copying files from the current directory, but it is not used in this Dockerfile.
#COPY . .

WORKDIR /usr/react

# This line sets the working directory for the Docker image to /usr/react.
# We initially had it set at just usr/ and then usr/react/public at some point but they didn't work. 

EXPOSE 3000

# This line exposes port 3000 to allow incoming traffic to the application running inside the container.

RUN apk update && apk upgrade && apk add curl

# This line updates the Alpine package index, upgrades installed packages, and installs the curl package.

RUN npm ci



RUN npm run build

CMD ["npm", "run", "start"]



#CMD ["npx", "serve", "build"]
```

This was the final build that worked but we (abby) tried a bunch of different commands. 

Such as changing the paths of the COPY, WORKDIR commands. 
The commented out command on line 23 was the original and we changed it to line 19 which was the final change that made it work. 
Each time we ran `docker build -t react-app .`
followed by  `docker run -p 3000:3000 react-app` which exposed the port we set in the Dockerfile to the port of the internal service. 

