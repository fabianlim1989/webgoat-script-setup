#!/bin/bash
# Remember to whitelist only known IP address / CIDR to access this instance!
echo "Remember to whitelist only known IP address / CIDR to access this instance!"
# This script can be used as the 'userdata' in the AWS CloudFormation to spin up
sudo yum -y update

# Get java and wget
sudo yum -y install java wget
cd /tmp
wget https://s3.amazonaws.com/webgoat-war/webgoat-container-7.0-SNAPSHOT-war-exec.jar
java -jar webgoat-container-7.0-SNAPSHOT-war-exec.jar

# Go to <$IP_ADDRESS>:8080/WebGoat, it should return HTTP 200 OK
curl localhost:8080/WebGoat/login.mvc -v

