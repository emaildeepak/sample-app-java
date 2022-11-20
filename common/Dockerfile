FROM openjdk:11-jre-slim
WORKDIR /var/lib/jenkins/workspace/
COPY --from=build /var/lib/jenkins/workspace/ common-0.9.0-SNAPSHOT.jar app.jar /var/lib/jenkins/workspace/ common-0.9.0-SNAPSHOT.jar app.jar
EXPOSE 50050
ENTRYPOINT ["java","-jar","common-0.9.0-SNAPSHOT.jar"]
