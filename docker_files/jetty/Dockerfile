FROM jetty:9.4.18-jre11

LABEL maintainer="iv.istvan.varga@gmail.com"
ENV JAVA_OPTIONS="-Xmx1g" 
USER jetty
COPY sample.war /var/lib/jetty/webapps/ROOT.war
