FROM openjdk:8-jre-alpine

ENV SPRING_OUTPUT_ANSI_ENABLED=ALWAYS \
    APP2_SLEEP=0 \
    JAVA_OPTS=""

CMD ./mvnw package
ADD /target/app-2-0.0.1-SNAPSHOT.war /app.war

EXPOSE 8082
CMD echo "The application will start in ${APP2_SLEEP}s..." && \
    sleep ${APP2_SLEEP} && \
    java ${JAVA_OPTS} -Djava.security.egd=file:/dev/./urandom -jar /app.war
