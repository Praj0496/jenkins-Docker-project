pipeline {
  agent none
  stages {
    stage('Back-end') {
      agent {
        docker {
          image 'maven:3.8.1-adoptopenjdk-11'
          reuseNode true                           // After the pipeline is finished, the Docker container will be stopped but not removed.This allows you to      
                                                   // inspect the container after the pipeline execution. 
        }
      }
      steps {
        // To Print Maven version
        sh 'mvn --version'
        
        // Build stage example: Build the project and download dependencies 
        // sh 'mvn clean install -DskipTests'
        
        // Example: Run unit tests
        //sh 'mvn test'
        
        // Example: Package the application
        //sh 'mvn package'
        
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
        docker {
          image 'node:16-alpine'
          reuseNode true                // After the pipeline is finished, the Docker container will be stopped but not removed.This allows you to      
                                                   // inspect the container after the pipeline execution.
        }
      }
      steps {
        // To print node version
        sh 'node --version'

        // Example: Install dependencies
        // sh 'npm install'

        // Example: Build the project
        //sh 'npm run build'

        // Example: Run tests
        //sh 'npm test'

        // Print a simple message
        echo 'Front-end build and tests completed successfully!'
      }
    }
  }
}
```

With `reuseNode true`, the Docker container will be reused for each stage that declares the same Docker image. After the pipeline is finished, the Docker container will be stopped but not removed. You can then list the containers using the `docker ps -a` command on your instance. If you have any other questions, feel free to ask! 😊
