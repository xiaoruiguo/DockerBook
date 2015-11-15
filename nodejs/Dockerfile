FROM ubuntu:14.04
MAINTAINER xiaoruiguo sean.xiao@pcitc.com
ENV REFRESHED_AT 2014-6-1
RUN apt-get -yqq update
RUN apt-get -yqq install nodejs npm
#RUN apt-get -yqq install curl
#RUN curl https://www.npmjs.com/install.sh | sh
RUN ln -s /usr/bin/nodejs /usr/bin/node
RUN mkdir -p /var/log/nodeapp


ADD nodeapp /opt/nodeapp

WORKDIR /opt/nodeapp
RUN npm install

VOLUME ["/var/log/nodeapp"]

EXPOSE 3000

ENTRYPOINT ["nodejs","server.js"]
