FROM openjdk:11-jre-slim
ARG WORKDIR="/usr/src/myapp"
RUN mkdir -p ${WORKDIR}
WORKDIR ${WORKDIR}
COPY target/request-0.0.1-SNAPSHOT.jar app.jar
EXPOSE 50050
#CMD ["java","-Dspring.profiles.active=dev","-jar","app.jar"]

ENV JAVA_OPTIONS=""


RUN printf "#!/bin/sh\nexec java \${JAVA_OPTIONS} \${@} -jar app.jar\n" > entrypoint.sh && chmod 755 entrypoint.sh
ENTRYPOINT [ "/usr/src/myapp/entrypoint.sh" ]
