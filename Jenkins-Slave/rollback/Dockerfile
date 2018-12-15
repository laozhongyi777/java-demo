FROM ubuntu

ENV JAVA_HOME /usr/local/jdk
ENV PATH=${JAVA_HOME}/bin

RUN mkdir -p /usr/share/jenkins
COPY kubectl.config /tmp/config
COPY kubectl /usr/bin/kubectl
COPY slave.jar /usr/share/jenkins/slave.jar  
COPY jenkins-slave /usr/bin/jenkins-slave

ENTRYPOINT ["jenkins-slave"]
