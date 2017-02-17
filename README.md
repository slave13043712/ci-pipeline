# Jenkins Docker Configuration

## Overview
Simple docker configuration for [Jenkins](https://jenkins.io/) and [SonarQube](https://www.sonarqube.org/).

## Getting Started
1. Clone this repository;
2. Run:
```
docker compose up
```
3. Access SonarQube at *localhost:9000* (deafult credentials are *admin*:*admin*)
4. Navigate to *Administration -> System -> Update Center*
5. Install the following plugins:
 * *Git*
 * *Java*
6. Navigate to  *Administration -> My Account -> Security* and generate server authentication token
7. Access Jenkins at *localhost:8080*
8. Navigate to *Jenkins -> Manage Jenkins -> Manage Plugins*
9. Install the following plugins:
 * *Git plugin*
 * *SonarQube Plugin*
10. Navigate to *Jenkins -> Manage Jenkins -> Global Tool Configuration*
11. Check *Install automatically* for SonarQube Scanner and Maven installations
12. Navigate to *Jenkins -> Manage Jenkins -> Configure System*
12. In *SonarQube servers* section specify *http://sonarqube:9000* as a *Server URL* and *Server authentication token*
13. Create your projects and have fun.

