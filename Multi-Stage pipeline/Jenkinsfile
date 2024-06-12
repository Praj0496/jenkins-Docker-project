pipeline {
  agent none
  stages {
    stage('Back-end') {
      agent {
        docker { image 'node:16-alpine' }
      }
      steps {
        sh 'node --version'
      }
    }
    stage('Front-end') {
      agent {
        docker { image 'maven:3.8.1-adoptopenjdk-11' }
      }
      steps {
        sh 'mvn --version'
      }
    }
    stage('Build Docker Image') {
      agent any
      steps {
        script {
          // Build the Docker image
          def appImage = docker.build("web-app", "-f 'Multi-Stage pipeline/Dockerfile' .")

          // Run the Docker container, exposing port 80
          appImage.run("-p 80:90 --name my-webapp-container")
        }
      }
    }
  }
}
