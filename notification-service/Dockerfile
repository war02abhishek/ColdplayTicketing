FROM openjdk:11-jdk-slim
WORKDIR /app
COPY build/libs/notification-service-0.0.1-SNAPSHOT.jar app.jar
EXPOSE 8083
ENTRYPOINT ["java", "-jar", "app.jar"]
