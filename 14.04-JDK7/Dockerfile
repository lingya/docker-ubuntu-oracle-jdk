FROM ubuntu:14.04
MAINTAINER lingya

RUN echo debconf shared/accepted-oracle-license-v1-1 select true | debconf-set-selections
RUN echo debconf shared/accepted-oracle-license-v1-1 seen true | debconf-set-selections

RUN apt-get update && \
    apt-get install -y --no-install-recommends software-properties-common && \
    add-apt-repository ppa:webupd8team/java && \
    apt-get update && \
    apt-get install -y --no-install-recommends oracle-java7-installer=7u76+7u60arm-0~webupd8~0
RUN apt-get install -y wget
RUN apt-get install -qq -y \
    python2.7-dev \
    pypy-dev
run apt-get clean && \
    rm -rf /var/cache/apt/archives/* /var/lib/apt/lists/*
