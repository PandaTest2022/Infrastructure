ARG DEBIAN_FRONTEND=noninteractive
FROM jenkins/ssh-agent:4.2.1-jdk11
USER root 
RUN apt-get update && apt-get install -y curl git python3 python3-pip
# Group ID is taken from the group ID set on host.
RUN groupadd -g 997 docker \
    && usermod -aG docker jenkins \
    && curl -fsSL https://get.docker.com/ | sh

RUN apt-get update && apt-get install -y unzip ansible

