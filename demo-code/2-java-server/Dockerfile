FROM ubuntu:16.04

RUN apt-get update
RUN apt-get install -y openjdk-7-jdk
RUN apt-get install -y gradle

RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure

COPY app /app

WORKDIR /app

RUN gradle :build

CMD gradle :tomcatRun

EXPOSE 8080
