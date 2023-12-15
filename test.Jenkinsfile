pipeline {
    agent any

    stages {
        stage('Read File') {
            steps {
                script {
                   /* def fileContent = readFile 'C:/ProgramData/Jenkins/.jenkins/workspace/JenkinsTestSetupData/Ruleset.xml'
                    echo "File Content: ${fileContent}"*/
                    sh 'wget https://github.com/pmd/pmd/releases/download/pmd_releases%2F6.49.0/pmd-bin-6.49.0.zip'
                    sh 'unzip pmd-bin-6.49.0.zip'

                    // Run PMD analysis
                    sh './pmd-bin-6.49.0/bin/run.sh pmd -d src -f text -R rulesets/java/quickstart.xml'
                }
            }
        }
    }
}
