FROM ubuntu:16.04
MAINTAINER cc-man
#添加python的安装包
ADD  Python-3.5.0.tar.xz /opt 
#更新apt
RUN  apt-get update && apt-get install -y 
 #安装依赖
RUN  apt-get install gcc -y && apt-get install make -y \
		&& apt-get install vim -y && apt-get install openssl -y \
		&& apt-get install libssl-dev -y && apt-get install python3-pip -y
RUN   ./opt/Python-3.5.0/configure --prefix=/usr/local/python3.5 \
		&& make && make install
RUN mkdir /opt/myApp/
VOLUME ["/opt/myApp/"]
CMD [""]


