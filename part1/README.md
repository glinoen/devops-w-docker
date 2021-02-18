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

## 1.6
```
docker build -t docker-clock .

docker container run docker-clock
```

## 1.7
```
docker container run -it curler
```

## 1.8
```
touch dogs.txt
docker container run -v "$(pwd)/dogs.txt:/usr/app/logs.txt" devopsdockeruh/first_volume_exercise
Wrote to file /usr/app/logs.txt
Wrote to file /usr/app/logs.txt
Wrote to file /usr/app/logs.txt
ctrl + c
cat dogs.txt
Wed, 03 Feb 2021 12:50:20 GMT
Wed, 03 Feb 2021 12:50:23 GMT
Wed, 03 Feb 2021 12:50:26 GMT
Wed, 03 Feb 2021 12:50:29 GMT
Secret message is:
"Volume bind mount is easy"
```

## 1.9
```
docker run -p 3567:80 devopsdockeruh/ports_exercise

"Ports configured correctly!!"
```

## 1.10
```
docker build -t frontendexampledocker .
docker run -p 5000:5000 frontendexampledocker
```

## 1.11
```
docker build -t backenddocker .
docker container run -v "$(pwd)/logs.txt:/usr/src/app/logs.txt" -p 8000:8000 backenddocker
```

## 1.12
```
docker build -t frontend12 .
docker run -p 5000:5000 frontend12

docker build -t backend12 .
docker run -p 8000:8000 backend12
```

## 1.13
```
docker image build -t springdocker .
docker run -p 8080:8080 springdocker
```

## 1.14
```
docker image build -t dockclicker .
docker run -p 3000:3000 dockclicker
```

## 1.15
https://hub.docker.com/r/kontittaja/tsoha-places
```
docker run -p 5000:5000 kontittaja/tsoha-places
```
open browser: localhost:5000

## 1.16
```
docker pull devopsdockeruh/heroku-example
docker tag devopsdockeruh/heroku-example registry.heroku.com/docker-exercise1-16/web
heroku login
heroku container:login
docker image push registry.heroku.com/docker-exercise1-16/web
heroku container:release -a docker-exercise1-16 web
```
https://docker-exercise1-16.herokuapp.com/
