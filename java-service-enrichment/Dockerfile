FROM bellsoft/liberica-openjdk-alpine:21

WORKDIR /app

COPY jar/java-service-enrichment.jar app.jar

EXPOSE 8080

ENTRYPOINT ["java", "-jar", "app.jar"]