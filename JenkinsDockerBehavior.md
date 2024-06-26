In Jenkins, when using Docker agents in a pipeline, the default behavior is to automatically remove the Docker containers after they have completed their tasks. 
This behavior is designed to clean up the environment and free up system resources.
The reuseNode true option reuses the Jenkins workspace for each stage that declares the same Docker image, but it doesn’t prevent Jenkins from removing the Docker containers.
While you can modify many aspects of how Jenkins interacts with Docker using various options in the Jenkinsfile, this particular behavior (automatic removal of Docker containers) 
is built into Jenkins and cannot be changed through the Jenkinsfile or Jenkins system configuration.
It’s important to note that while this behavior might seem limiting, it is actually a good practice in most cases. 
Containers are meant to be ephemeral and disposable, and cleaning up stopped containers helps to ensure that your system doesn’t get cluttered with unused resources. 
