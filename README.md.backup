# docker
Docker and Kubernetes - Full Course for Beginners AmigosCode
remove origin!!


add our new origin, to our github:
```
git remote add origin git@github.com:bullitjose/docker
```


add changes at local to origin, at github:

```
git push -u origin master
```

download changes at github to local:

```
git pull origin master

git and github
```

   …or create a new repository on the command line:

```
echo "# testing" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/bullitjose/testing.git
git push -u origin main
```

    …or push an existing repository from the command line:

```
git remote add origin https://github.com/bullitjose/testing.git
git branch -M main
git push -u origin main
```

>Install Docker Desktop

Recommended approach to install Docker Desktop on Ubuntu:
   1.Set up Docker's package repository. See step one of Install using the apt repository.

   2.Download latest DEB package: [install using the repository](https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository)

   3.Install the package with apt as follows:
   
```
 sudo apt-get update

 sudo apt-get install ./docker-desktop-<version>-<arch>.deb
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

> I opened the terminal to run and i got this error:

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

>0009 Docker Images and Containers

How to use this image (wordpress):

[images from hub docker](https://hub.docker.com/_/wordpress)
```
$ docker run --name some-wordpress --network some-network -d wordpress
```
If you'd like to be able to access the instance from the host without the container's IP, standard port mappings can be used:
```
$ docker run --name some-wordpress -p 8080:80 -d wordpress
Unable to find image 'wordpress:latest' locally
latest: Pulling from library/wordpress
b0a0cf830b12: Pull complete 
c93478d47932: Pull complete 
e74cc574d0d2: Pull complete 
e4782e138a90: Pull complete 
cfeec87621ae: Pull complete 
c1badcd002c0: Pull complete 
e0d463a60cb6: Pull complete 
8bce13a727be: Pull complete 
8cbeca1cab87: Pull complete 
9216544a8100: Pull complete 
2b3680ee4acb: Pull complete 
35fa048d3ad4: Pull complete 
e8be4124e519: Pull complete 
7f1beb739060: Pull complete 
fa118a71e862: Pull complete 
2769eb42fecf: Pull complete 
0e93a2a8bf0f: Pull complete 
638e00bd0917: Pull complete 
513bffc3d60d: Pull complete 
ea7798d3fbb1: Pull complete 
f2eb955eba32: Pull complete 
Digest: sha256:9ce0773fc5be134b2a2268ccc9e1da8cf9b17a0462259a38a2c85e604c9c02cd
Status: Downloaded newer image for wordpress:latest
e70c38d95942eb39ebc4307268bc48732c9b7befc426bf72dcd51d4dd8c5ec34

```
 Search at internet:
 ```
 http://localhost:8080
 ```
 we run wordpress on our machine.
 
 
 > running container, docker ps:
 ```
  $docker ps -a                  
  ```
                            
|CONTAINER ID|   IMAGE       |COMMAND                  |CREATED         |STATUS         |PORTS                  |NAMES|
|----|---|---|---|---|---|---|
|e70c38d95942   |wordpress   |"docker-entrypoint.s…"   |9 minutes ago   |Up 9 minutes   |0.0.0.0:8080->80/tcp   |some-wordpress|


>stop contanier, docker stop:

```
$docker stop e70c38d95942
e70c38d95942
$docker ps -a            
CONTAINER ID   IMAGE       COMMAND                  CREATED          STATUS                     PORTS     NAMES
e70c38d95942   wordpress   "docker-entrypoint.s…"   10 minutes ago   Exited (0) 2 seconds ago             some-wordpress

```

>remove container, docker rm:

```
$docker rm e70c38d95942  
e70c38d95942
$docker ps -a           
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
```
>remove container without stopp it, docker rm -f:

```
$docker rm 00d353764328             
Error response from daemon: cannot remove container "/some-wordpress": container is running: stop the container before removing or force remove
$docker rm -f 00d353764328
00d353764328
$docker ps -a             
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
```

>0011 Docker ps format
use a Go template Pretty-print containers:

```
docker ps --help

Usage:  docker ps [OPTIONS]

List containers

Aliases:
  docker container ls, docker container list, docker container ps, docker ps

Options:
  -a, --all             Show all containers (default shows just running)
  -f, --filter filter   Filter output based on conditions provided
      --format string   Format output using a custom template:
                        'table':            Print output in table format with column headers (default)
                        'table TEMPLATE':   Print output in table format using the given Go template
                        'json':             Print in JSON format
                        'TEMPLATE':         Print output using the given Go template.
                        Refer to https://docs.docker.com/go/formatting/ for more information about formatting output with templates
  -n, --last int        Show n last created containers (includes all states) (default -1)
  -l, --latest          Show the latest created container (includes all states)
      --no-trunc        Don't truncate output
  -q, --quiet           Only display container IDs
  -s, --size            Display total file sizes
```

To get the nicely formatted docker, here is the string:
```
$export FORMAT="ID\t{{.ID}}\nNAME\t{{.Names}}\nIMAGE\t{{.Image}}\nPORTS\t{{.Ports}}\nCOMMAND\t{{.Command}}\nCREATED\t{{.CreatedAt}}\nSTATUS\t{{.Status}}\n" 
```
Now we use this format:
```
$ docker ps --format=$FORMAT
ID	6dbfbdf677a9
NAME	some-wordpress
IMAGE	wordpress
PORTS	0.0.0.0:8080->80/tcp
COMMAND	"docker-entrypoint.s…"
CREATED	2024-05-14 12:53:57 +0200 CEST
STATUS	Up About a minute
```







