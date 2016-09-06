# Jenkins-golang

* [Docker Hub]

## Components

* Base: Ubuntu **14.04**
* Jenkins (version: **latest**)
* Go (version: **1.7**)

## Running & Building

### Running

```sh
$ docker run --name=jenkins --rm -it -p 8005:8080 -p 2205:22 -p 50005:50000 -v $(pwd)/var/jenkins_home:/var/jenkins_home pitchanon/jenkins-golang 
```

Run container in background

```sh
$ docker run --name=jenkins --rm -it -d -p 8005:8080 -p 2205:22 -p 50005:50000 --restart=always -v $(pwd)/var/jenkins_home:/var/jenkins_home pitchanon/jenkins-golang 
```

### Building

```sh
$ docker-compose up --build -d
```

### Localhost
* [Jenkins url]

[Docker Hub]: https://hub.docker.com/r/pitchanon/jenkins-golang/
[Jenkins url]: http://localhost:8005
