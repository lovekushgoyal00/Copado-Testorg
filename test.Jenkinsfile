pipeline {
    agent any

    stages {
        stage('Read File') {
            steps {
                script {
                    def fileContent = readFile 'C:\\ProgramData\\Jenkins\\.jenkins\\workspace\\JenkinsTestSetupData\\objects\\Account.object'
                    echo "File Content: ${fileContent}"
                }
            }
        }
    }
}
