# Part 1

## 1.1 
```
CONTAINER ID   IMAGE     COMMAND                  CREATED          STATUS                      PORTS     NAMES
0134efef8649   nginx     "/docker-entrypoint.…"   32 seconds ago   Exited (0) 13 seconds ago             charming_hopper
f4e6638fd98d   nginx     "/docker-entrypoint.…"   39 seconds ago   Exited (0) 7 seconds ago              brave_goldberg
f2d7cc37ba87   nginx     "/docker-entrypoint.…"   52 seconds ago   Up 50 seconds               80/tcp    nostalgic_ptolemy
```

## 1.2
```
docker container ls -a
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
```
```
docker image ls
REPOSITORY   TAG       IMAGE ID   CREATED   SIZE
```

## 1.3
```
Give me the password: basics
You found the correct password. Secret message is:
"This is the secret message"
```

## 1.4
```
docker exec -it ba bash
root@ba5e02676aae:/usr/app# tail -f ./logs.txt
"Docker is easy"
Thu, 28 Jan 2021 09:13:21 GMT
Thu, 28 Jan 2021 09:13:24 GMT
Thu, 28 Jan 2021 09:13:27 GMT
Thu, 28 Jan 2021 09:13:30 GMT
Secret message is:
"Docker is easy"
Thu, 28 Jan 2021 09:13:36 GMT
Thu, 28 Jan 2021 09:13:39 GMT
Thu, 28 Jan 2021 09:13:42 GMT
Thu, 28 Jan 2021 09:13:45 GMT
```

## 1.5
```
docker container run -it  ubuntu sh -c 'apt-get update; apt-get install curl; echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website;'
```