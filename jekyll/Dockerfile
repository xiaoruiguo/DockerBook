FROM ubuntu:14.04
MAINTAINER xiaoruiguo ruiguo.xiao@gmail.com
RUN apt-get -yqq update
RUN apt-get -yqq install python-software-properties
RUN apt-get -yqq install software-properties-common
RUN apt-add-repository ppa:brightbox/ruby-ng
RUN apt-get -yqq update
RUN apt-get -yqq install ruby2.1 ruby2.1-dev make nodejs
RUN gem sources -r https://rubygems.org/
RUN gem sources -a https://ruby.taobao.org
RUN gem install --no-rdoc --no-ri jekyll
VOLUME [ "/data/", "/var/www/html" ]
WORKDIR /data
ENTRYPOINT [ "jekyll", "build", "--destination=/var/www/html" ]

