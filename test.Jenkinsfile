pipeline {
    agent any

    stages {
        stage('Read File') {
            steps {
                script {
                   /* def fileContent = readFile 'C:/ProgramData/Jenkins/.jenkins/workspace/JenkinsTestSetupData/Ruleset.xml'
                    echo "File Content: ${fileContent}"*/
                    def command ='C:/ProgramData/Jenkins/.jenkins/workspace/JenkinsTestSetupData/Ruleset.xml'

                    sh command
                }
            }
        }
    }
}
