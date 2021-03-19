#### Task 1.2 
We’ve left containers and a image that won’t be used anymore and are taking space, as `docker ps -as` and docker images will reveal.
Clean the docker daemon from all images and containers.
Submit the output for `docker ps -a` and `docker images`.

#### Solution
```
lintukoto:~ sonjaek$ docker ps -a
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES

lintukoto:~ sonjaek$ docker images
REPOSITORY   TAG       IMAGE ID   CREATED   SIZE
```
