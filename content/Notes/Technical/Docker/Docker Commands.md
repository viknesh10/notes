## Getting started

- Create an empty [[Dockerfile]] in the directory
```
touch Dockerfile
```
- Add the following contents
```
FROM node:18-alpine
WORKDIR /app
COPY . .
RUN yarn install --production
CMD ["node", "src/index.js"]
EXPOSE 3000
```
- The [[FROM]] command from Dockerfile instructs the builder to start from node:18-alpine image. And since that image was not available readily, it had to be downloaded (downloads happen during the docker build command execution) 
- The [[WORKDIR]] command then sets the directory out for the next command - COPY. COPY is followed by . . -> which specifies that the source and destination respectively are the same target directories (or folders) - in this case, /app.
- The yarn command installs dependencies and the [[CMD]] specifies the default command to run when starting a container from this image.
- Build the image in the same directory
```
docker build -t <tag-name> .
```
- The docker build command uses the Dockerfile to build a new image. 
- The -t flag tags the image followed by the tag-name which is just a human readable name for the final image.
	- This tag-name can be referred to when you run the container
- Run your container using the following command
```
docker run -dp 127.0.0.1:3000:3000 <tag-name>
```
- The -d flag runs the container in the background. This means that Docker starts your container and returns you to the terminal
	- The -d flag stands for --detach
- The -p flag creates a port mapping between the host and the container.
	- The -p flag stands for --publish
- The -p flag takes a string value in the format of HOST:CONTAINER, where HOST is the address on the host and CONTAINER is the port on the container.
	- The command publishes port 3000 (the container's port) to 127.0.0.1:3000 on the host.
```
docker ps
```
- The above command is used to list out the running containers.

## Update the application

- To re-build your image or to update the version of the image, use the same build command as stated in the Getting Started section.
- Get container id
```
docker ps
```
- Stop running container
```
docker stop <container-id>
```
- Removing the old container
```
docker rm <container-id>
```

## Persistance

- Create a volume:
```
docker volume create <volume-name>
```
- Mount the volume in your container
```
docker run -dp 127.0.0.1:3000:3000 --mount type=volume,src=<volume-name>,target=<volume-target> <tag-name>
```
- The --mount flag allows you to specify a volume mount. 
- You can inspect the volume using the following command
```
docker volume inspect <volume-name>
```
- This will enable you to see where Docker is storing your data when you use a volume.

