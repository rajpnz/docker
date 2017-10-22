# Stage 1. Clone Git
FROM alpine/git as clone
WORKDIR /app
RUN git clone https://github.com/rajpnz/springboot.git

# Stag 2. Do the Maven install
FROM maven:3.5-jdk-8-alpine as build
WORKDIR /app
COPY --from=clone /app/springboot /app
RUN mvn install

# Stage 3 Run the artifact
FROM openjdk:8-jre-alpine
WORKDIR /app
# Make port 8090 available to the world outside this container
EXPOSE 8090
COPY --from=build /app/target/springboot-0.0.1-SNAPSHOT.jar /app
ENTRYPOINT ["sh", "-c"]
CMD ["java -jar springboot-0.0.1-SNAPSHOT.jar"]

