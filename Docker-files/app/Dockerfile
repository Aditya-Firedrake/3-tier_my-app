From maven:3.9.9-eclipse-temurin-21-jammy AS BUILD_IMAGE
RUN git cone https://github.com/hkhcoder/vprofile-project.git
RUN cd vprofile-project && checkout containers && mvn install


FROM tomcat:10-jdk21
LABEL "project"="vprofile"
LABEL "author"="aditya"
RUN rm -rf usr/local/tomcat/webapps/*
COPY --from=BUILD_IMAGE vprofile-project/target/vprofile-v2.war /usr/local/tomcat/webapps/ROOT.war

EXPOSE 8080
CMD ["catalina.sh", "run"]