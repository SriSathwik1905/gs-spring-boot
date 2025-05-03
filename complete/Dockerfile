# Use an official OpenJDK runtime as a parent image
FROM openjdk:17-jdk-slim

# Set the working directory in the container
WORKDIR /app

# Copy thefat jar file into the container at /app
# Note: The JAR filename depends on the pom.xml (artifactId-version.jar)
# Check your target/ directory after 'mvn package' to confirm the exact name
# Usually it's something like target/gs-spring-boot-0.1.0.jar
COPY target/*.jar app.jar

# Make port 8080 available to the world outside this container
EXPOSE 8080

# Run the jar file
ENTRYPOINT ["java","-jar","/app/app.jar"]