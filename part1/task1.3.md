#### Task
Image `devopsdockeruh/simple-web-service:ubuntu` will start a container that outputs logs into a file. 
Go inside the container and use `tail -f ./text.log` to follow the logs. 
Submit the secret message and command(s) given as your answer.

#### Solution
```
lintukoto:~ sonjaek$ docker run -d -it --name secret devopsdockeruh/simple-web-service:ubuntu

Unable to find image 'devopsdockeruh/simple-web-service:ubuntu' locally
ubuntu: Pulling from devopsdockeruh/simple-web-service
5d3b2c2d21bb: Pull complete 
3fc2062ea667: Pull complete 
75adf526d75b: Pull complete 
965d4bbb586a: Pull complete 
4f4fb700ef54: Pull complete 
Digest: sha256:d44e1dce398732e18c7c2bad9416a072f719af33498302b02929d4c112e88d2a
Status: Downloaded newer image for devopsdockeruh/simple-web-service:ubuntu
6e8087bf110b4374a2e8c026a837aadec4460eebb385713dceb72d0c31cf9001
```
```
lintukoto:~ sonjaek$ docker exec -it secret bash
root@6e8087bf110b:/usr/src/app# tail -f ./text.log

2021-03-19 11:16:00 +0000 UTC
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
2021-03-19 11:16:02 +0000 UTC
...
```
```
lintukoto:~ sonjaek$ ^p^q

read escape sequence
```
