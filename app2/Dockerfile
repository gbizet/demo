FROM openjdk:8-jre-alpine

ENV SPRING_OUTPUT_ANSI_ENABLED=ALWAYS \
    APP2_SLEEP=0 \
    JAVA_OPTS=""

ADD *.war /app.war

EXPOSE 8082
CMD echo "The application will start in ${APP2_SLEEP}s..." && \
    sleep ${APP2_SLEEP} && \
    java ${JAVA_OPTS} -Djava.security.egd=file:/dev/./urandom -jar /app.war
