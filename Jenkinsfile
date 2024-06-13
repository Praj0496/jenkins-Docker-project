pipeline {
  agent none
  stages {
    stage('Back-end') {
      agent {
        docker { image 'maven:3.8.1-adoptopenjdk-11' }
      }
      steps {
        // To Print Maven version
        sh 'mvn --version'

        // Build the project and download dependencies
        sh 'mvn clean install -DskipTests'
        
        // Run unit tests
        sh 'mvn test'
        
        // Package the application
        sh 'mvn package'
      }
    }
    stage('Front-end') {
      agent {
        docker { image 'node:16-alpine' }
      }
      steps {
        // To print node version
        sh 'node --version'

        // Install dependencies
        sh 'npm install'

        // Build the project
        sh 'npm run build'

        // Run tests
        sh 'npm test'
      }
    }
  }
}
