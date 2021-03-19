### Task 1.4
Start a ubuntu image with the process `sh -c 'echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website;'`
You will notice that a few things required for proper execution are missing. Be sure to remind yourself which flags to use so that the read actually waits for input.
Test inputting `helsinki.fi` into the application. This time return the command you used to start process and the command(s) you used to fix the ensuing problems.

#### Solution
```
lintukoto:~ sonjaek$ docker run -d -it --name missing ubuntu

Unable to find image 'ubuntu:latest' locally
latest: Pulling from library/ubuntu
5d3b2c2d21bb: Already exists 
3fc2062ea667: Already exists 
75adf526d75b: Already exists 
Digest: sha256:b4f9e18267eb98998f6130342baacaeb9553f136142d40959a1b46d6401f0f2b
Status: Downloaded newer image for ubuntu:latest
89cd7996904615535b33591ff3154617df04f44c778c029eba80fbc9a6c23503
```
```
lintukoto:~ sonjaek$ docker exec -it missing bash
root@89cd79969046:/# apt update

...
```
```
root@89cd79969046:/# apt upgrade

...
```
```
root@89cd79969046:/# apt install curl

...
```
```
root@89cd79969046:/# sh -c 'echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website;'

Input website:
helsinki.fi

Searching..
<!DOCTYPE HTML PUBLIC "-//IETF//DTD HTML 2.0//EN">
<html><head>
<title>301 Moved Permanently</title>
</head><body>
<h1>Moved Permanently</h1>
<p>The document has moved <a href="http://www.helsinki.fi/">here</a>.</p>
</body></html>
```
