# on Windows:
# $ docker run --name jenkins --restart unless-stopped -u root -p 8080:8080 -p 50000:50000 afuscella/abap-ci
#
# on Unix:
# $ docker run --name jenkins --restart unless-stopped -u root -p 8080:8080 -p 50000:50000 -v jenkins-data:/var/jenkins_home -v /var/run/docker.sock:/var/run/docker.sock afuscella/abap-ci

FROM jenkins/jenkins:lts
MAINTAINER Arthur Silva <arthur.silva@sap.com>

USER root

RUN apt-get update 

RUN curl -sL https://deb.nodesource.com/setup_10.x | bash -
RUN apt-get install -y nodejs

RUN npm install -g newman

RUN mkdir -p /var/www/jenkins
RUN chown jenkins /var/www/jenkins

ENV JENKINS_HOME="/var/www/jenkins"
ENV JENKINS_USER="jenkins"

WORKDIR /var/www/jenkins

USER jenkins