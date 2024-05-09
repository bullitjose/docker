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


