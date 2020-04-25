# jenkins-configuration-as-code

This project demonstrates configuring and running Jenkins using configuration as code.
The Jenkins is built using docker, hence docker is pre-requite.

### Pre-requisite
- Docker

### Build docker image

Go to master dir and run following command

`$ docker build -t jenkins-casc:latest .`

### Spin up Jenkins

User below command to spin up Jenkins container

`$ docker run -p 8080:8080 --rm jenkins-casc:latest`

### Access Jenkins

Open URL `http://localhost:8080` in browser
