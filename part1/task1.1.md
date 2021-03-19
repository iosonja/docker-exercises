#### Task 1.1 
Start 3 containers from image that does not automatically exit, such as nginx, detached.
Stop 2 of the containers leaving 1 up.
Submit the output for `docker ps -a` which shows 2 stopped containers and one running.

#### Solution
```
lintukoto:~ sonjaek$ docker ps -a

CONTAINER ID   IMAGE     COMMAND                  CREATED              STATUS                       PORTS     NAMES
d250d1403c64   nginx     "/docker-entrypoint.…"   About a minute ago   Exited (0) 20 seconds ago              keen_mirzakhani
4ab6d4c4b871   nginx     "/docker-entrypoint.…"   About a minute ago   Exited (0) 7 seconds ago               flamboyant_newton
656a7a3506bf   nginx     "/docker-entrypoint.…"   About a minute ago   Up About a minute            80/tcp    loving_davinci
```
