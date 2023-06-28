---
title: CI/CD
date: 2021-02-16 10:12:11
tags: Maven build up the java application
reference: https://www.jenkins.io/zh/doc/tutorials/build-a-java-app-with-maven/#run-jenkins-in-docker
---

1.install Docker
  P1:WSL2 installation is incomplete
     ->install WSL 2 linux kernel
       ->https://docs.microsoft.com/zh-cn/windows/wsl/install-win10#step-4---download-the-linux-kernel-update-package
2. running jenkins in docker with jenkins linux container image
   P1. Error response from daemon: \Users\jiang%!(EXTRA string=is not a valid Windows path).
     ->englich version-https://www.jenkins.io/doc/book/installing/docker/#setup-wizard
       Run a docker:dind Docker image
       docker run --name jenkins-docker --rm --detach `
         --privileged --network jenkins --network-alias docker `
          --env DOCKER_TLS_CERTDIR=/certs `
          --volume jenkins-docker-certs:/certs/client `
           --volume jenkins-data:/var/jenkins_home `
        docker:dind

       int the thrid step with ` replacing ^  in PowerShell
   P2. manifest for jenkins:latest not found: manifest unknown: manifest unknown.
       "Tag number" should be searched out in Jenkins hub

    P3. check out the password for Unlock Jenkins  
         docker logs -f jenkins_name 
         docker exec -it  jenkins:2.60.3 bash

         $ docker run -p "(local)7070":8080 -p 50000:50000 jenkins/jenkins


https://github.com/docker/labs/blob/master/beginner/chapters/setup.md


download docker in disk D



Installing Jenkins with Docker doc.


