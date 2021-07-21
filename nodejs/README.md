# Docker for Node.js

This is a docker file for setting up a dev environment for Node.js

### Instructions
Copy the Dockerfile to Node.js code folder and run:
```
docker build -t <image primary name>:<image sub name> .
docker run -p 3001:3001 --rm --name <container name> <image primary name>:<image sub name>
```

To list all the containers, including the inactive ones, run:
```
docker ps -a
```

To list all the images, run:
```
docker images
```

To stop & remove the container, run:
```
docker stop <container name>
```

To remove the images, run:
```
docker rmi <image primary name>:<image sub name> node:14
```

To run the container with volume, run:
```
docker run -p 3001:3001 --rm --name <container name> -v <volume name>:<internal container path> <image primary name>:<image sub name>
```

To list the volumes, run:
```
docker volume ls
```

To clear all anonymous volumes, run:
(they are not removed by default when --rm flag was false)
```
docker volume prune
```