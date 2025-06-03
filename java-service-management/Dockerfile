FROM bellsoft/liberica-openjdk-alpine:21

WORKDIR /app

COPY jar/java-service-management.jar app.jar

EXPOSE 8081

ENTRYPOINT ["java", "-jar", "app.jar"]