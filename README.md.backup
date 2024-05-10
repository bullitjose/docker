# docker
Docker and Kubernetes - Full Course for Beginners AmigosCode
remove origin!!


add our new origin, to our github

git remote add origin git@github.com:bullitjose/docker

add changes at local to origin, at github
```
git push -u origin master
```

download changes at github to local
```
git pull origin master

git and github
```

    …or create a new repository on the command line
```
echo "# testing" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/bullitjose/testing.git
git push -u origin main
```

    …or push an existing repository from the command line
```
git remote add origin https://github.com/bullitjose/testing.git
git branch -M main
git push -u origin main
```

>Launch Docker Desktop

To start Docker Desktop for Linux, search Docker Desktop on the Applications menu and open it. This launches the Docker menu icon and opens the Docker Dashboard, reporting the status of Docker Desktop.

Alternatively, open a terminal and run:
```
 systemctl --user start docker-desktop
 ```
 
 After you’ve successfully installed Docker Desktop, you can check the versions of these binaries by running the following commands:
```
 docker compose version
Docker Compose version v2.17.3

 docker --version
Docker version 23.0.5, build bc4487a

 docker version
Client: Docker Engine - Community
 Cloud integration: v1.0.31
 Version:           23.0.5
 API version:       1.42
<...>
```

> I opened the terminal to run and igot this error:

```
systemctl --user start docker-desktop

Failed to start docker-desktop.service: Unit docker-desktop.service is masked
```

The solution is to unmask the service and enable it.

Solution:
```
$ file /etc/xdg/systemd/user/docker-desktop.service
```

Running the command above, you should notice that the file is a symlink to /dev/null

Delete the file: $ sudo rm /etc/xdg/systemd/user/docker-desktop.service

And then enable the service for the user: $ systemctl --user enable docker-desktop

> 0005_Exploring Docker Dashboard


>0006_Tools

>0007_Getting Started with Docker

>0008_Undestanding Containers

![docker cheatsheet](dockercheatsheet8.png)

>Basic Docker CLIs

|Command| 	Description|
|----|---|
|docker run| 	Run a command in a new container|
|docker build| 	Build an image from a Dockerfile|
|docker push| 	Push an image to a registry|
|docker pull| 	Pull an image from a registry|
|docker stop|	Stop a running container|
|docker rm|	Remove one or more containers|


>Container Management CLIs

|Command| 	Description|
|----|---|
|docker create image[command]| create the container|
|docker run image[command]|	= create + start|
|docker start container...| 	start the container|
|docker stop container...| graceful2 stop|
|docker kill container...|kill (SIGKILL) the container|
|docker restart container... | = stop + start|
|docker pause container...|Suspend the container|
docker unpause container...|Resume the container|
|docker wait container...| 	Block until one or more containers stop, then print their exit codes|
|docker top container...| 	Display the running processes of a container|
|docker rm[-f]container...|	destroy the container|

>Inspecting The Container

Here’s the list of the basic Docker commands that helps you inspect the containers seamlessly:

|Command| 	Description|
|----|---|
|docker ps| 	list running container|
|docker ps -a| 	list all containers|
|docker logs [-f] |container	Show the container output(stdout+stderr)|
|docker diff container| 	Show the differences with the image (modified files)|
|docker top container...| 	Display the running processes of a container|
|docker inspect --format='{{ .Config.Image }}' my_container_name..|	Inspect a container and extract specific information using --format: |


>Interacting with Container

|Command| 	Description|
|----|---|
|docker attach container	|attach to a running container(stdin/stdout/stderr)|
|docker cp container:path hostpath |copy files from the container|
|docker cp hostpath - container: path|copy files into the container|
|docker export container|	export the content of the container (tar archive)|
|docker exec container args ... 	|run a command in an existing container (useful for debugging)|
|docker wait container... 	|wait until the container terminates and return the exit code|
|docker commit container image 	|commit a new docker image (snapshot of the image)|

>Image Management Commands

|Command| 	Description|
|----|---|
|docker images	|list all local images|
|docker history |image show the image history(list of ancestors)|
|docker inspect image... |show level-info's(in json format)|
|docker tag image tag	|tag an image|
|docker commit container image 	|Create an image(from a container)|
|docker import url -[tag] 	|Create an image(from a tarball)|
|docker rmi image...	|delete images|

>Image Transfer Commands

|Using the registry API| 	Description|
|----|---|
|docker push repo[:tag]...	|push an image /repository from a registry|
|docker pull repo[:tag]..	|pull an image /repository from a registry|
|docker search text	|search an image on the official registry|
|docker login... 	|login to a registry|
|docker logout... 	|logout from a registry|
|docker export <container_id> >image.tar 	|exporting: You can export a Docker image as a tarball file using the docker export command
|docker import image image.tar <image_name>:<tag>|importing: On the target system, you can import the Docker image from the tarball using the docker import command|

|Manual Transfer| 	Description|
|----|---|
|docker save repo [:tag]... 	|export an image/repo as a tarball|
|docker load	|load images from a tarball|
|docker-ssh |proposed script to transfer images between two daemons over ssh |

>Builder Main Commands

|Command| 	Description|
|----|---|
|FROM image|scratch	|base image for the build|
|MAINTAINER email	|name of the maintainer(metadata).|
|COPY path dst 	|copy path from the context into the container at location destination(dst)|
|ADD src dst 	|same as COPY but untar archives and accepts https urls|
|RUN args.. 	|run an arbitrary command 1inside the container
|USER name	|set the default username1
|WORKDIR path	|set the default working directory|
|CMD args.. 	|set the default command|
|ENV name value	|set an environment variable|
