FROM openjdk:11-jre-slim
WORKDIR="/usr/src/myapp"
RUN mkdir -p ${WORKDIR}
WORKDIR ${WORKDIR}
COPY target/common-0.9.0-SNAPSHOT.jar app.jar
EXPOSE 50050

ENV JAVA_OPTIONS=""


RUN printf "#!/bin/sh\nexec java \${JAVA_OPTIONS} \${@} -jar app.jar\n" > entrypoint.sh && chmod 755 entrypoint.sh
ENTRYPOINT [ "/usr/src/myapp/entrypoint.sh" ]
