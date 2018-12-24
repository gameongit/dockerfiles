ARG  CODE_VERSION=latest
FROM centos:${CODE_VERSION}
MAINTAINER Lalitsharma
RUN yum update -y
RUN yum install -y java-1.8.0-openjdk-devel curl vim
RUN curl --silent --location http://pkg.jenkins-ci.org/redhat-stable/jenkins.repo | tee /etc/yum.repos.d/jenkins.repo
RUN rpm --import https://jenkins-ci.org/redhat/jenkins-ci.org.key
RUN yum install jenkins -y
RUN systemctl enable jenkins 
EXPOSE 81/tcp
ENTRYPOINT systemctl start jenkins && bash
