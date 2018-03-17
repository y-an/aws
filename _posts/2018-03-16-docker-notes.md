---
title: Docker Notes
---

* TOC
{:toc}

from  0:00 to 26:00
-----

1. pulls nginx image from docker
    > docker pull nginx
2. run nginx container from image with custom name and port 9999 (which maps to 80 inside port)
    > docker container run -p 9999:80 --name web-server nginx:latest
3. see list of containers running
    > docker ps
4. stop specific container by id orname
    > docker stop [id/name]
5. start interactive bash with container
    > docker exec -it web-server /bin/bash
6. bash commands inside container
    ```
    cd usr
    cd share
    cd nginx
    cd html
    ls -la
    touch page.html # creates page
    apt-get update
    apt-get install -y nano
    nano page.html
    ```
    2. CTRL + X -> "Y" -> Enter (confirm file name)

7. list all containers (including exited)
    > docker ps -a

8. remove container by id/name    
    > docker rm web-server

9. run container and soon as container stops, remove it from list of containers
    > docker container run -p 9999:80 --name web-server --rm nginx:latest 

10. run container with volume mapping (must share drive from app)
    > docker container run -p 9999:80 --name web-server --rm -v c:/docker-notes/nginx/html:/usr/share/nginx/html nginx:latest 

11. create Dockerfile (capital "D")
```dockerfile
FROM nginx:latest
EXPOSE 80
RUN apt-get update && apt-get install -y nano
LABEL maintainer="email@address.com"
VOLUME /usr/share/nginx/html
```

12. create image (note last argument, period, for current location)
    > docker build -t web-server .  # this create image, not instance

13. list images
    > docker image ls

14. run container from image (note last argument changed from nginx)
    > docker container run --name web-server --rm -p 9999:80 web-server:latest
