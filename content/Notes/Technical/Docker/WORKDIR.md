- The WORKDIR instruction sets the working directory for any of the commands that follow it like RUN, COPY, CMD, ENTRYPOINT, etc
- If the command doesnt exist in [[Dockerfile]], it will be created automatically
	- If a directory is not specified, the default is /
	- But if you're creating a Dockerfile from Scratch, the WORKDIR might be set by the base image you are using.
		- Hence the best practice is to set your WORKDIR explicitly to avoid unintended operations.
- The WORKDIR command can be used multiple times in a Dockerfile.
```
WORKDIR /a
WORKDIR b
WORKDIR c
RUN pwd
```
- In this scenario, the final output of pwd would be /a/b/c
- The WORKDIR can resolve environment variables previously set using ENV.
	- This is only applicable to ENV variables which are  explicitly set in Dockerfiles