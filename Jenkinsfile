pipeline {
    agent any // This specifies that the pipeline can run on any available agent (Jenkins slave).

    stages {        
        stage('Build') {
            steps {
                // Perform the build steps, e.g., compile your code.
                sh 'docker build -t khalilsellamii/tp2-docker .'
            }
        }

        stage('Tag') {
            steps {
                // Run tests for your application.
                sh 'docker tag khalilsellamii/tp2-docker khalilsellamii/tp2-docker:v1.0'
            }
        }

        stage('Login') {
            steps {
                // Run tests for your application.
                sh 'docker login -u khalilsellamii -p Khalil3456'
            }
        }

        stage('Push') {
            steps {
                // Deploy your application to your target environment.
                sh 'docker push khalilsellamii/tp2-docker:v1.0'
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
