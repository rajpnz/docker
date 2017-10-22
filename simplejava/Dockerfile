# Base Alpine Linux based image with OpenJDK JRE only
FROM openjdk:8-jre-alpine

# Set the working directory to /app
WORKDIR /app

# Copy the current directory contents into the container at /app
ADD . /app

# Install any needed packages specified in requirements.txt
RUN env

# Make port 80 available to the world outside this container
EXPOSE 80

# Define environment variable
ENV NAME World

# Run the back to work jar  when the container launches
# https://github.com/rajpnz/maven-java.git
CMD ["java", "-cp", "back2work-0.0.1-SNAPSHOT.jar", "nz.co.rajees.back2work.Example"]
