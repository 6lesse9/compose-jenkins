FROM ubuntu:20.04

RUN apt-get update && apt-get install git -y
RUN apt-get install default-jdk -y 
RUN DEBIAN_FRONTEND=noninteractive apt-get install maven -y

RUN git clone https://github.com/shephertz/App42PaaS-Java-MySQL-Sample.git /tmp/sample
WORKDIR /tmp/sample
RUN mvn package

RUN mkdir /tmp/target && cp /tmp/sample/App42PaaS-Java-MySQL-Sample.war /tmp/target