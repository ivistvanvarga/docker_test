
FROM centos:7
ARG CONT_IMG_VER
ENV CONT_IMG_VER ${CONT_IMG_VER:-v1.0.0}
ENV MYUSER jbossuser
ENV MYUSER_UID 1005
ENV MYUSER_GROUP jbossuser
ENV MYUSER_GID 1005
ENV MYUSER_HOME /home/jbossuser

LABEL maintainer="iv.istvan.varga@gmail.com"
WORKDIR ${MYUSER_HOME}
RUN groupadd -g ${MYUSER_GID} ${MYUSER_GROUP} && useradd -g ${MYUSER_GID} -u ${MYUSER_UID} -d ${MYUSER_HOME} -m  ${MYUSER}

COPY Dockerfile /Dockerfile
RUN yum update -y && yum install -y epel-release && yum install -y java-1.8.0-openjdk-headless java-1.8.0-openjdk java-1.8.0-openjdk-accessibility && yum clean all
USER ${MYUSER}

ENTRYPOINT top -b
