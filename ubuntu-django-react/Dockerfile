FROM ubuntu:16.04

MAINTAINER togglecorp info@togglecorp.com

RUN apt-get update && \
    apt-get install -y \
        git \
        locales \
        vim \
        curl \
        unzip \
        python3 \
        python3-dev \
        python3-setuptools \
        python3-pip

RUN locale-gen en_US.UTF-8
ENV LANG en_US.UTF-8

RUN pip3 install uwsgi

RUN curl -sL https://deb.nodesource.com/setup_6.x | bash -
RUN apt-get install -y nodejs

RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add -
RUN echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list
RUN apt-get update && apt-get install yarn

RUN rm -rf /var/lib/apt/lists/*
