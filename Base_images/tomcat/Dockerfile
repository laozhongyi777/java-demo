FROM ubuntu
MAINTAINER lizhenliang

ENV VERSION=8.5.31

ENV JAVA_HOME /usr/local/jdk

RUN apt-get update && \
    apt-get install wget curl unzip iproute2 net-tools -y && \
    apt-get clean all && \
    wget http://mirrors.shu.edu.cn/apache/tomcat/tomcat-8/v${VERSION}/bin/apache-tomcat-${VERSION}.tar.gz && \
    tar zxf apache-tomcat-${VERSION}.tar.gz && \
    mv apache-tomcat-${VERSION} /usr/local/tomcat && \
    rm -rf apache-tomcat-${VERSION}.tar.gz /usr/local/tomcat/webapps/* && \
    sed -i '1a JAVA_OPTS="-Djava.security.egd=file:/dev/./urandom"' /usr/local/tomcat/bin/catalina.sh && \
    ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime

WORKDIR /usr/local/tomcat

EXPOSE 8080
CMD ["./bin/catalina.sh", "run"]
