FROM tomcat:latest

ADD ./webapp /usr/local/tomcat/webapps/ROOT

RUN sed -i -e 's/8080/3000/' conf/server.xml

EXPOSE 3000

CMD ["catalina.sh", "run"]
