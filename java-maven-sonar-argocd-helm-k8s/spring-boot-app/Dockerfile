# Use the same base image
FROM adoptopenjdk/openjdk11:alpine-jre

# Install cifs-utils for SMB mounts
RUN apk add --no-cache cifs-utils

# Simply the artifact path
ARG artifact=target/spring-boot-web.jar

WORKDIR /opt/app

COPY ${artifact} app.jar

# This should not be changed
ENTRYPOINT ["java","-jar","app.jar"]
