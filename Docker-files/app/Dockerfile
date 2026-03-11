FROM  maven:3.9.9-eclipse-temurin-21 as mvn_build

RUN git clone -b containers --single-branch https://github.com/hkhcoder/vprofile-project.git

RUN cd vprofile-project && mvn install



FROM tomcat:10-jdk-21

RUN rm -rf /usr/local/tomcat/webapps/*

COPY --from=mvn_build /vprofile-project/target/vprofile-v2.war /usr/local/tomcat/webapps/root.war

EXPOSE 8080

CMD ["catalina.sh","run"]
