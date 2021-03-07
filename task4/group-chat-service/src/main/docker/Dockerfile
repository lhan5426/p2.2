# JDK 8 base image
FROM openjdk:8-jre-alpine

#no package manager in this os...

# Open port 80
EXPOSE 80

# Copy the files from the host file system and ADD them to the desired directory inside the container image
# Note that this will copy the JAR to `/demo-1.0-SNAPSHOT-jar-with-dependencies.jar`
ADD ./target/spring-chat-0.1.0.jar /

# Define the command which runs when the container starts
# Note that the filepath of the JAR is `/demo-1.0-SNAPSHOT-jar-with-dependencies.jar`
# as in the filesystem of the image,
# NOT `./target/demo-1.0-SNAPSHOT-jar-with-dependencies.jar` as in the host filesystem
CMD ["java -jar spring-chat-0.1.0.jar"]

# Use Bash as the container's entry point.
ENTRYPOINT ["/bin/sh", "-c"]
