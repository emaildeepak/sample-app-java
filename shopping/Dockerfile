FROM openjdk:11-jre-slim
COPY target/shopping-0.9.0-SNAPSHOT.jar app.jar
RUN mkdir -p /shopping/incoming/ /shopping/outgoing/ /shopping/reports/
EXPOSE 50050
CMD ["java","-Dspring.profiles.active=dev","-jar","app.jar"]
