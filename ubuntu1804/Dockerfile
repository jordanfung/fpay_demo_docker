from ubuntu:18.04

RUN apt-get update -y
RUN apt-get install -y build-essential libcereal-dev libgflags-dev libgoogle-glog-dev libhiredis-dev libtinyxml-dev libssl-dev git redis-server python unzip

## for slow network
#COPY master.zip /
#RUN unzip master.zip
#WORKDIR /fpay_demo-master

## for fast network
RUN git clone https://github.com/jordanfung/fpay_demo.git
WORKDIR /fpay_demo

RUN ./setup.sh
