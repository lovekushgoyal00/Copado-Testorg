pipeline {
    agent any

    stages {
        stage('Install Docker') {
            steps {
                script {
                    sh 'sudo apt-get update'
                    sh 'sudo apt-get install -y docker.io'
                }
            }
        }

        stage('Build and Publish') {
            steps {
                // Your build and publish steps here
            }
        }
    }
}
