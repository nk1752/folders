# pull ubuntu 20.04 base image
FROM ubuntu:22.04

RUN apt-get update

# install curl
RUN apt install curl -y


RUN apt-get update

RUN cd ~
RUN echo "************** download nodesource_setup **************"
RUN curl -sL https://deb.nodesource.com/setup_20.x -o nodesource_setup.sh
RUN chmod +x nodesource_setup.sh

RUN bash nodesource_setup.sh

RUN echo "************** install npm & nodejs **************"
RUN apt-get install nodejs -y && apt-get update

# check node version
RUN echo "************** Checking NEW Node Version **************"
RUN node -v
# check npm version
RUN echo "************** Checking NEW NPM Version **************"
RUN npm -v