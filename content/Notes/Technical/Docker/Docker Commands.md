# Getting started
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