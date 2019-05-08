FROM centos:7
ENV MYUSER jbossuser
ENV MYUSER_UID 1005
ENV MYUSER_GROUP jbossuser
ENV MYUSER_GID 1005
ENV MYUSER_HOME /home/jbossuser

LABEL maintainer="iv.istvan.varga@gmail.com"
WORKDIR ${MYUSER_HOME}
RUN groupadd -g ${MYUSER_GID} ${MYUSER_GROUP} && useradd -g ${MYUSER_GID} -u ${MYUSER_UID} -d ${MYUSER_HOME} -m  ${MYUSER}

COPY Dockerfile /Dockerfile

USER ${MYUSER}

ENTRYPOINT top -b
