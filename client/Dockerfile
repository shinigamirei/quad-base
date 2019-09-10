#Use a base node image
FROM node AS build-env

#copy contents into image
WORKDIR /quad-base_client_build
copy . .
#execute command to download dependancies
# execute command to construct node project
run npm install
run npm run build

ENTRYPOINT ["npm","start"]
# use a new image
FROM node
# copy through the build directory created in a previous step
WORKDIR /quad-base_client
COPY --from=build-env /quad-base_client_build .
# run the command to download dependacies - but append it with -g serve
run npm install -g serve
# create an entrypoint instruction - it will take 3 arguments "serve"(make sure you get the correct location), "-l", and a port number
EXPOSE 3000
ENTRYPOINT ["serve","-l","3000"]
