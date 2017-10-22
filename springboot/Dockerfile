# Base Alpine Linux based image with OpenJDK JRE only
FROM openjdk:8-jre-alpine

# Set the working directory to /app
WORKDIR /app

# Copy the current directory contents into the container at /app
ADD . /app

# Install any needed packages specified in requirements.txt
RUN env

# Make port 8090 available to the world outside this container
EXPOSE 8090

# Define environment variable
ENV NAME World

# Run the springboot  jar  when the container launches
# https://github.com/rajpnz/springboot.git
CMD ["java", "-jar", "springboot-0.0.1-SNAPSHOT.jar"]
