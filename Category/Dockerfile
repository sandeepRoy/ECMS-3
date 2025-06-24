# Use Java 17 image
FROM openjdk:17-jdk-slim

# Create a directory inside the container
WORKDIR /app

# Copy the built jar file into container
COPY target/*.jar category.jar

# Run the jar
ENTRYPOINT ["java", "-jar", "category.jar"]

