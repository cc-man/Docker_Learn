FROM ubuntu:16.04 
MAINTAINER cc-man
#上传
ADD apache-tomcat-7.0.82.tar.gz /opt/tomcat
ADD jdk-7u80-linux-x64.tar.gz /opt/jdk
COPY /run.sh /root/run.sh
RUN  chmod 777 /root/run.sh
#环境变量
ENV JAVA_HOME=/opt/jdk/jdk1.7.0_80/jre
ENV PATH=:$JAVA_HOME/bin:$PATH
ENV CLASSPATH=.:$JAVA_HOME/lib:$JAVA_HOME/lib/tools.jar
ENTRYPOINT ["/root/run.sh"]

