FROM openjdk:11-jre-slim
RUN mkdir apps
COPY target/delivery-0.9.0-SNAPSHOT.jar.original  /apps
WORKDIR /apps
EXPOSE 50050
ENTRYPOINT ["java", "-jar", "delivery-0.9.0-SNAPSHOT.jar.original"]
