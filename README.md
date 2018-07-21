
# FefoCloud AppSec
Test DevSecOps

## Folder Structure
|Folder|Description|
|---|---|
|[pipeline](pipeline)| Jenkinsfiles responsible for application deploy|
|[images](images)| Base images to devtools application|


```sh
$ git clone https://github.com/leandrodma/fefocloud.gi
$ cd fefocloud/images/jenkinsWithDocker/
```
Second build the jenkins with docker image
```sh 
$ sudo docker build -t fefocloud/jenkins:1.0 .
```
Third executing the container with [Docker](http://docker.io) and [Jenkins](http://jenkins.io)

```sh
sudo docker container run --name jenkins -d --restart=always -p 8080:8080 -p 50000:50000 -u 0 -v jenkins_home:/var/jenkins_home fefocloud/jenkins:1.0
```
