# Docker_file_creation, Github and Docker_Hub_Integration 

# steps:

- first create new folder and open in vs code.
- create a py file named helloworld.py and print("Hello world")
- then create dockerfile with no extension named docker_file
- Use some commands in new_dockerfile, which are as follow:
- FROM python:3 (to set base image for the container and specifies the "python" with the version tag "3")
- WORKDIR (To set the working directory for any command)
- COPY (To copy files and directories from the build to container)
- CMD (To specity the default command that should be executed when the container starts)

# Dependencies
- Python interpreter
- docker/dockerhub
- git/github

# To Build the docker image
#steps:
- Open the command prompt to the same directory which contains python and dockerfile
- docker build -f docker_file -t hello-app (Use to build the docker image, -f for indicate the name of dockerfile and -t tags the image with name hello-app)
- docker run hello-app (Use print the output "Hello world" in command prompt and it confirms that python app is running in container)
- docker images (To show the list of images created)

# To push the image to your dockerhub
#steps:
- open the command prompt
- docker tag image_name docker_hub_username/image_name (before push, tag the image to docker hub)
- docker login (To login your docker hub account with login command)
- docker push docker_hub_username/image_name (To push the tagged image to your docker hub)

# To push the codebase into GitHub repo, steps & commands are mention below:
- firsst create the repo on github, named it and create it
- copy the https address of repo
- then go to folder where py and dockerfile, enter cmd in location bar
- git init (To initialize the empty repo)
- git remote add origin github_repo_url (To add the remote origin of given address)
- git add . (To stage the changes in working dir for the commit)
- git commit -m "message" (To tracked the file)
- git push origin main (To push the codebase into github repo)
