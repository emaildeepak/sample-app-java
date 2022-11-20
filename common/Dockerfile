
FROM openjdk:11-jre-slim
EXPOSE 50050
ARG JAR_FILE=target/common-0.9.0-SNAPSHOT.jar
ADD ${common-0.9.0-SNAPSHOT.jar} app.jar
ENTRYPOINT ["java","-jar","/app.jar"]
