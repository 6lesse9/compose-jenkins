FROM ubuntu:20.04

RUN sudo apt-get update && apt-get install git -y
RUN sudo apt-get install default-jdk -y 
RUN sudo apt-get install maven -y

RUN git clone https://github.com/shephertz/App42PaaS-Java-MySQL-Sample.git /tmp/sample
WORKDIR /tmp/sample
RUN mvn package

RUN sudo mkdir /tmp/target && cp /tmp/sample/App42PaaS-Java-MySQL-Sample.war /tmp/target