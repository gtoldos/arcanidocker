FROM ubuntu:latest
RUN apt-get update -y
RUN apt-get install clang libicu-dev -y

#Download the latest binary release

RUN cd && mkdir swift
RUN apt-get install wget
RUN wget https://swift.org/builds/swift-3.1-release/ubuntu1610/swift-3.1-RELEASE/swift-3.1-RELEASE-ubuntu16.10.tar.gz

#import the PGP keys into your keyring:

RUN wget -q -O - https://swift.org/keys/all-keys.asc | gpg --import -

#First, refresh the keys to download new key revocation certificates, if any are available:

RUN gpg --keyserver hkp://pool.sks-keyservers.net --refresh-keys Swift


RUN gpg --verify swift-3.1-RELEASE-ubuntu16.10.tar.gz.sig
RUN tar xzf swift-3.1-RELEASE-ubuntu16.10.tar.gz

RUN $ export PATH=$(pwd)/swift-3.1-RELEASE-ubuntu16.10/usr/bin:"${PATH}"

RUN apt-get install -y build-essential -y
RUN curl -sL https://deb.nodesource.com/setup_6.x | -E bash -
RUN apt-get install -y nodejs -y


