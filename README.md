# Jenkins Docker Configuration

## Overview
Simple [docker](https://www.docker.com/) configuration for [Jenkins](https://jenkins.io/) and [SonarQube](https://www.sonarqube.org/).

## Getting Started
1. Clone this repository;
2. Run:
```
docker-compose up
```

### Configure SonarQube
1. Access SonarQube at *localhost:9000* (deafult credentials are *admin*:*admin*)
2. Navigate to *Administration -> System -> Update Center*
3. Install the following plugins:
 * *Git*
 * *Java*
4. Navigate to  *Administrator -> My Account -> Security* and generate server authentication token

### Configure Jenkins
1. Access Jenkins at *localhost:8080*
2. Navigate to *Jenkins -> Manage Jenkins -> Manage Plugins*
3. Install the following plugins:
 * *Git plugin*
 * *SonarQube Plugin*
4. Navigate to *Jenkins -> Manage Jenkins -> Global Tool Configuration*
5. Check *Install automatically* for SonarQube Scanner and Maven installations
6. Navigate to *Jenkins -> Manage Jenkins -> Configure System*
7. In *SonarQube servers* section specify *http://sonarqube:9000* as a *Server URL* and *Server authentication token*
8. Create your projects (use `/var/jenkins_home/workspace/$JOB_NAME/` as path in job configuration) and have fun.

