FROM ubuntu:latest
MAINTAINER Vladimir Shakhov <vladimir.shakhov.tomsk@gmail.com>
COPY static-server /home/srv
RUN apt-get update && apt-get install curl -y
RUN cd ~ && curl -sL https://deb.nodesource.com/setup_6.x -o nodesource_setup.sh && bash nodesource_setup.sh && apt-get install nodejs
RUN cd /home/srv/ && npm install
CMD cd /home/srv/ && nodejs static-server.js
