# Implementation of a DevOps Pipeline for a Web Application using Jenkins and Docker
Jenkins- Docker Integration

**Project Description**:

In this project, I designed and implemented a comprehensive DevOps pipeline for a web application using Jenkins and Docker. The pipeline was hosted on an EC2 instance with an Ubuntu image and was divided into distinct stages for handling the back-end and front-end builds separately.

Key responsibilities and achievements include:

1. **Environment Setup**: Configured an EC2 instance with Ubuntu and installed Jenkins and Docker to create a robust environment for the DevOps pipeline.

2. **Pipeline Design**: Designed a Jenkins pipeline with two stages: 'Back-end' and 'Front-end'. Each stage used a Docker agent with a specific image ('maven:3.8.1-adoptopenjdk-11' for the back-end and 'node:16-alpine' for the front-end) to ensure isolated and consistent environments for the builds.

3. **Pipeline Execution**: Executed various commands in each stage to demonstrate the build process. This included printing the Maven and Node.js versions, displaying the current working directory, and listing its contents.

4. **Container Management**: Leveraged the `reuseNode true` option in Jenkins to ensure that Docker containers were not removed after their tasks were completed, allowing for post-execution inspection.

This project demonstrates my proficiency in Jenkins and Docker, and my ability to design and implement effective DevOps pipelines. It showcases real-world application as it mirrors the process that many development teams follow to automate the build and deployment of their applications. By separating the back-end and front-end builds into different stages and using Docker to ensure consistent build environments, this project reflects best practices in DevOps and containerization. 
