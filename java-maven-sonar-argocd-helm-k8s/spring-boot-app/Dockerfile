# You can change this base image to anything else
# But make sure to use the correct version of Java
FROM adoptopenjdk/openjdk11:alpine-jre

# Simply the artifact path
ARG artifact=target/spring-boot-web.jar

WORKDIR /opt/app

COPY ${artifact} app.jar

# This should not be changed
##ENTRYPOINT ["java","-jar","app.jar"]
ENTRYPOINT ["java","-jar","app.jar", ">", "/opt/app/logs/app.log", "2>&1"]
