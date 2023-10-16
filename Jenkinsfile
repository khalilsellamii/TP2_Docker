pipeline {
    agent any // This specifies that the pipeline can run on any available agent (Jenkins slave).

    stages {
        stage('Checkout') {
            steps {
                // This step checks out your source code from your version control system (e.g., Git).
                script {
                    git 'https://github.com/khalilsellamii/TP2_Docker'
                }
            }
        }
        
        stage('Build') {
            steps {
                // Perform the build steps, e.g., compile your code.
                echo "this is the build phase"
            }
        }

        stage('Test') {
            steps {
                // Run tests for your application.
            sh 'python3 src/test.py'
            }
        }

        stage('push') {
            steps {
                // Deploy your application to your target environment.
                sh 'this is the push phase '
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
