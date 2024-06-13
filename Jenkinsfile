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
        
        // Print the current working directory
        sh 'pwd'

        // List the contents of the current directory
        sh 'ls -la'

        // Print a simple message
    echo 'Back-end build and tests completed successfully!'
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

        // Print a simple message
        echo 'Front-end build and tests completed successfully!'
      }
    }
  }
}
