pipeline {
    agent any

    stages {
        stage('Git Clone') {
            steps {
                // Checkout the code from the Git repository
                git 'https://github.com/lovekushgoyal00/Copado-Testorg.git'
            }
        }

        stage('Install Docker') {
            steps {
                // Your Docker installation steps here
                // Make sure to use Windows-compatible commands
                bat 'echo Docker installation steps go here'
            }
        }

    }
}
