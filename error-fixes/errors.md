# Docker custom machine is not running

ISSUE : `Error getting IP address: Host is not running`

`$ docker-machine ls`  

NAME          | Active       | Driver | STATE | URL | SWARM | DOCKER    | ERRORS
------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | -------------
shivani-k8s-demo   | -        | virtualbox   | Saved   |      |        |   | Unknown   


`$ docker-machine ip shivani-k8s-demo`

Error getting IP address: Host is not running

`$ docker-machine active`

No active host found

`$ docker-machine start shivani-k8s-demo`

```
Starting "shivani-k8s-demo"...
(shivani-k8s-demo) Waiting for an IP...
Machine "shivani-k8s-demo" was started.
Waiting for SSH to be available...
Detecting the provisioner...
Started machines may have new IP addresses. You may need to re-run the `docker-machine env` command.
```

`$ docker-machine env shivani-k8s-demo`

```
export DOCKER_TLS_VERIFY="1"
export DOCKER_HOST="tcp://192.168.99.100:2376"
export DOCKER_CERT_PATH="/Users/shivani.singhal/.docker/machine/machines/shivani-k8s-demo"
export DOCKER_MACHINE_NAME="shivani-k8s-demo"
//Run this command to configure your shell: 
// eval $(docker-machine env shivani-k8s-demo)
```

`$ docker-machine ls`

NAME          | Active       | Driver | STATE | URL | SWARM | DOCKER    | ERRORS
------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | -------------
shivani-k8s-demo   | -        | virtualbox   | Running   |    tcp://192.168.99.100:2376   |        | v19.03.5   | Unknown   

docker machine `shivani-k8s-demo` status changed from saved to running.

`$ docker-machine ip shivani-k8s-demo`

192.168.99.100
