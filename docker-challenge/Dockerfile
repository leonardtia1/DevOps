FROM tomcat:latest

MAINTAINER Tia M

RUN rm -rf /usr/local/tomcat/webapps/*

COPY ./pebble.war /usr/local/tomcat/webapps

WORKDIR /usr/local/tomcat/conf
RUN sed -i '/tomcat-users/a <user username="admin" password="admin" roles="manager-gui, manager-script, manager-jmx, manager-status"/>' tomcat-users.xml

EXPOSE 8080
CMD ["catalina.sh", "run"]
