# ====== Stage 1: Build the JAR ======
FROM maven:3.9.6-eclipse-temurin-17 AS build
WORKDIR /app
COPY . .
RUN mvn clean package -DskipTests

# ====== Stage 2: Run the app ======
FROM openjdk:17-jdk-slim
WORKDIR /app
COPY --from=build /app/target/*.jar configuration.jar
ENTRYPOINT ["java", "-jar", "configuration.jar"]

