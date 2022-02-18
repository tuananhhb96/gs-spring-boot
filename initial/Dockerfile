FROM maven:3.8.4-jdk-8 AS build
WORKDIR /app
COPY pom.xml .
COPY . .

RUN mvn clean install
FROM maven:3.8.4-jdk-8

## Package stage#FROM openjdk:11-jre-slim
COPY --from=build /app/target/spring-boot-initial-0.0.1-SNAPSHOT.jar /usr/local/lib/spring-boot-initial-0.0.1-SNAPSHOT.jar
EXPOSE 8080
CMD ["java", "-jar", "/usr/local/lib/spring-boot-initial-0.0.1-SNAPSHOT.jar"]
