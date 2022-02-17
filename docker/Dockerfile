FROM openjdk:8-jdk-alpine
COPY . . 
RUN mvn clean install -DskipTests
CMD ["java", "-jar", "spring-boot-initial-0.0.1-SNAPSHOT.jar"]

