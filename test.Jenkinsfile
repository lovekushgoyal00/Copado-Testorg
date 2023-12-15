pipeline {
    agent any

    stages {
        stage('Read Current Directory Data') {
            steps {
                script {
                    def currentDirectory = sh(script: 'pwd', returnStdout: true).trim()
                    def fileContent = sh(script: 'cat Account.object', returnStdout: true).trim()

                    echo "Current Directory: ${currentDirectory}"
                    echo "File Content: ${fileContent}"
                }
            }
        }
    }
}
