options {
    skipDefaultCheckout true
}

stages {
    stage('Git Clone') {
        steps {
            script {
                // Explicitly checkout the desired branch
                checkout([$class: 'GitSCM', branches: [[name: 'refs/heads/main']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'your-credentials-id', url: 'https://github.com/lovekushgoyal00/Copado-Testorg.git']]])
            }
        }
    }

    // Your other stages here
}
