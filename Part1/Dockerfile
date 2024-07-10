# Start from the alpine image that is smaller but no fancy tools
#FROM alpine:3.19

# Use /usr/src/app as our workdir. The following instructions will be executed in this location.
#WORKDIR /usr/src/app

# Copy the hello.sh file from this directory to /usr/src/app/ creating /usr/src/app/hello.sh
#COPY hello.sh .

# Alternatively, if we skipped chmod earlier, we can add execution permissions during the build.
# RUN chmod +x hello.sh

#Execute a command with '/bin/sh -c' prefix
#RUN touch additional.txt  

# When running docker run the command will be ./hello.sh
#CMD ./hello.sh



# Start from ubuntu:22.04 base image
FROM ubuntu:22.04

# Update the package list and install curl
RUN apt-get update && apt-get install -y curl

# Copy the script file into the container
COPY script.sh /usr/local/bin/script.sh

# Make the script executable
RUN chmod +x /usr/local/bin/script.sh

# Set the command to run the script on container start
CMD ["/usr/local/bin/script.sh"]

