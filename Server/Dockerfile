FROM ubuntu:22.04 AS development

ENV TZ=Europe/Warsaw
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

RUN apt update && apt install -y build-essential unzip vim git curl wget zip
RUN apt-get install -y curl unzip zsh gradle default-jdk

RUN apt-get update &&\
	apt-get upgrade -y &&\
    apt-get install -y  software-properties-common

COPY . /gradle/src
WORKDIR /gradle/src
RUN gradle build

RUN chmod +x gradlew

EXPOSE 8080:8080
CMD ./gradlew run