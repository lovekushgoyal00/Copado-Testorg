pipeline {
    agent any

    stages {
        stage('Read File') {
            steps {
                script {
                    def fileContent = readFile 'object/Account.object'
                    echo "File Content: ${fileContent}"
                }
            }
        }
    }
}
