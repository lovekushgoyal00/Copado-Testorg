pipeline {
    agent any

    stages {
        stage('Install Docker') {
            steps {
                script {
                    // Update package list and install required dependencies
                    sh 'sudo apt-get update'
                    sh 'sudo apt-get install -y apt-transport-https ca-certificates curl software-properties-common'

                    // Add Docker GPG key
                    sh 'curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg'

                    // Set up stable Docker repository
                    sh 'echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null'

                    // Install Docker engine
                    sh 'sudo apt-get update'
                    sh 'sudo apt-get install -y docker-ce docker-ce-cli containerd.io'

                    // Add the Jenkins user to the docker group to run Docker commands without sudo
                    sh 'sudo usermod -aG docker $USER'
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
