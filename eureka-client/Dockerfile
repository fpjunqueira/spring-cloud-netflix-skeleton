# Start with a base image containing Java runtime
FROM openjdk:8-jdk-alpine

# Add Maintainer Info
LABEL maintainer="felipetiuzanata@gmail.com"

# Add a volume pointing to /tmp
VOLUME /tmp

# The application's jar file
ARG JAR_FILE=target/eureka-client-0.0.1-SNAPSHOT.jar

# Add the application's jar to the container
ADD ${JAR_FILE} eureka-client-0.0.1-SNAPSHOT.jar

# Run the jar file 
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/eureka-client-0.0.1-SNAPSHOT.jar"]