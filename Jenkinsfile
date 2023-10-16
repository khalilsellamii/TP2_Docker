stage('Build and Push Docker Image') {
    steps {
        script {
            // Define the Docker image name and tag.
            def dockerImage = "khalilsellamii/tp-docker:latest"
            
            // Build the Docker image from the Dockerfile.
            sh "docker build -t $dockerImage ."
            
            // Push the Docker image to Docker Hub.
            sh "docker push $dockerImage"
        }
    }
}