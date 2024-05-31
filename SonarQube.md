## Installation steps - SonarQube

**Method - 1:**
Running SonarQube as a docker container

**NOTE:** Docker installation required

```
docker run -d --name sonar -p 9000:9000 sonarqube:<version>

or

docker run -d --name sonar -p 9000:9000 sonarqube:lts-community
```
