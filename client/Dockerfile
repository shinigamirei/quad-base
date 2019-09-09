#Use a base node image
FROM node:latest

#copy contents into image
WORKDIR /Quad-Base_Client
copy . .
#execute command to download dependancies
# execute command to construct node project
run npm install

ENTRYPOINT ["npm","start"]
# use a new image

# copy through the build directory created in a previous step

# run the command to download dependacies - but append it with -g serve

# create an entrypoint instruction - it will take 3 arguments "serve"(make sure you get the correct location), "-l", and a port number
