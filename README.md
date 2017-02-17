# Jenkins Docker Configuration

## Overview
Simple docker configuration for [Jenkins](https://jenkins.io/) and [SonarQube](https://www.sonarqube.org/).

## Getting Started
1. Clone this repository;
2. Run:
```
docker compose up
```

### Configure SonarQube
1. Access SonarQube at *localhost:9000* (deafult credentials are *admin*:*admin*)
2. Navigate to *Administration -> System -> Update Center*
3. Install the following plugins:
 * *Git*
 * *Java*
4. Navigate to  *Administration -> My Account -> Security* and generate server authentication token
5. Access Jenkins at *localhost:8080*

### Configure Jenkins
1. Navigate to *Jenkins -> Manage Jenkins -> Manage Plugins*
2. Install the following plugins:
 * *Git plugin*
 * *SonarQube Plugin*
3. Navigate to *Jenkins -> Manage Jenkins -> Global Tool Configuration*
4. Check *Install automatically* for SonarQube Scanner and Maven installations
5. Navigate to *Jenkins -> Manage Jenkins -> Configure System*
6. In *SonarQube servers* section specify *http://sonarqube:9000* as a *Server URL* and *Server authentication token*
7. Create your projects and have fun.

