pipeline {
    agent any // This specifies that the pipeline can run on any available agent (Jenkins slave).

    stages {
        
        stage('Build') {
            steps {
                // Perform the build steps, e.g., compile your code.
                sh " docker ps"
            }
        }

        stage('Test') {
            steps {
                // Run tests for your application.
            sh 'echo "this is test phase"'
            }
        }

        stage('push') {
            steps {
                // Deploy your application to your target environment.
                sh 'echo "this is the push phase" '
            }
        }
    }

    post {
        success {
            // Actions to take when the pipeline succeeds (e.g., notify the team).
            echo 'The pipeline has succeeded!'
        }

        failure {
            // Actions to take when the pipeline fails (e.g., send an alert).
            echo 'The pipeline has failed!'
        }
    }
}
