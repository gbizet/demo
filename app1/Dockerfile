FROM openjdk:8-jre-alpine

ENV SPRING_OUTPUT_ANSI_ENABLED=ALWAYS \
    APP1_SLEEP=0 \
    JAVA_OPTS=""

ADD *.war /app.war

EXPOSE 8081
CMD echo "The application will start in ${APP1_SLEEP}s..." && \
    sleep ${APP1_SLEEP} && \
    java ${JAVA_OPTS} -Djava.security.egd=file:/dev/./urandom -jar /app.war
