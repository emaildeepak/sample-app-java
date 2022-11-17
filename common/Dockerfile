FROM openjdk:11-jre-slim
RUN mkdir /app
COPY target/common-0.9.0-SNAPSHOT.jar app.jar /app
WORKDIR /app
EXPOSE 50050
ENTRYPOINT ["java", "-jar", "common-0.9.0-SNAPSHOT.jar app.jar"]
