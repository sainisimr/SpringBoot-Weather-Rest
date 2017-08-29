FROM openjdk:8-jdk-alpine
VOLUME /tmp
ADD target/weather-api-0.0.1.jar app.jar
RUN sh -c 'touch /app.jar'
ENV JAVA_OPTS="-DSpring.profiles.active=prod"
ENTRYPOINT [ "sh", "-c", "java $JAVA_OPTS -Djava.security.egd=file:/dev/./urandom -jar /app.jar" ]