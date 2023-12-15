pipeline {
    agent any

    stages {
        stage('Install Docker') {
            steps {
                script {
                    // Install Docker dependencies
                    sh 'sudo apt-get update'
                    sh 'sudo apt-get install -y apt-transport-https ca-certificates curl software-properties-common'

                    // Add Docker GPG key
                    sh 'curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg'

                    // Set up stable Docker repository
                    sh 'echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null'

                    // Install Docker engine
                    sh 'sudo apt-get update'
                    sh 'sudo apt-get install -y docker-ce docker-ce-cli containerd.io'

                    // Add Jenkins user to the docker group
                    sh 'sudo usermod -aG docker $USER'
                }
            }
        }
    }
}
