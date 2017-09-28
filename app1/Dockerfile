FROM oracle/openjdk

ENV SPRING_OUTPUT_ANSI_ENABLED=ALWAYS \
    APP1_SLEEP=0 \
    JAVA_OPTS=""

CMD ./mvnw package
ADD target/microapp-1-0.0.1-SNAPSHOT.war /app.war

EXPOSE 8081
CMD echo "The application will start in ${APP1_SLEEP}s..." && \
    sleep ${APP1_SLEEP} && \
    java ${JAVA_OPTS} -Djava.security.egd=file:/dev/./urandom -jar /app.war
