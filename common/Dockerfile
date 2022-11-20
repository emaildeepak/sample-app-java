FROM maven as build
WORKDIR /app
COPY . .
RUN mvn install

FROM openjdk:11-jre-slim
WORKDIR /app
COPY --from=build /app/target/common-0.9.0-SNAPSHOT.jar app.jar /app/common-0.9.0-SNAPSHOT.jar app.jar
EXPOSE 50050
ENTRYPOINT ["java","-jar","common-0.9.0-SNAPSHOT.jar"]
