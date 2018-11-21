FROM ubuntu:18.04

RUN DEBIAN_FRONTEND=noninteractive apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y software-properties-common && rm -rf /var/lib/apt/lists/*
RUN add-apt-repository -y ppa:openjdk-r/ppa
RUN apt-get update && apt-get install -y openjdk-8-jdk openjdk-8-jre
RUN update-alternatives --config java
RUN update-alternatives --config javac
RUN apt-key adv --keyserver ha.pool.sks-keyservers.net --recv-keys 379CE192D401AB61
RUN echo "deb https://rundeck.bintray.com/rundeck-deb /" > /etc/apt/sources.list.d/rundeck.list
RUN DEBIAN_FRONTEND=noninteractive apt-get update && DEBIAN_FRONTEN=noninteractive apt-get install -y rundeck
RUN service rundeckd start &
