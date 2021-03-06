# Jenkins Golang

* [Docker Hub]

## Components

* Base: Ubuntu **14.04**
* Jenkins (version: **latest**)
* Go (version: **1.7**)

## Running & Building

### Running

```sh
$ docker run --name=jenkins --rm -it -p 8001:8080 -p 2201:22 -p 50001:50000 -v $(pwd)/var/jenkins_home:/var/jenkins_home -v $(pwd)/root/.ssh:/root/.ssh pitchanon/jenkins-golang 
```

Run container in background

```sh
$ docker run --name=jenkins -d -it -p 8001:8080 -p 2201:22 -p 50001:50000 --restart=always -v $(pwd)/var/jenkins_home:/var/jenkins_home -v $(pwd)/root/.ssh:/root/.ssh pitchanon/jenkins-golang 
```

### Building

```sh
$ docker build -t my-jenkins-app .
$ docker run --name jenkins -it --rm -p 8001:8080 -p 2201:22 -p 50001:50000 -v $(pwd)/var/jenkins_home:/var/jenkins_home -v $(pwd)/root/.ssh:/root/.ssh my-jenkins-app
```

### Docker Compose

```sh
$ docker-compose up --build -d
```

### Localhost
* [http://localhost:8001]

[Docker Hub]: https://hub.docker.com/r/pitchanon/jenkins-golang/
[http://localhost:8001]: http://localhost:8001
