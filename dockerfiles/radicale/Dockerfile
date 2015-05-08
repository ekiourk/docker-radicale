FROM debian:jessie
MAINTAINER Ilias Kiourktsidis <ekiourk@gmail.com>

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update -qq && apt-get upgrade -y -qq
RUN apt-get install -y python2.7 python-pip

# Install radicale through pip
RUN pip install radicale

ADD config /opt/radicale/config
 
EXPOSE 5232

CMD ["radicale"]