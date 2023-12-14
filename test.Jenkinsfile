pipeline {
    agent any
    
    tools {
        // Ensure 'docker' refers to the tool installation defined in Global Tool Configuration
        docker 'dockerTool'
    }

    stages {
        stage('Build and Push') {
            steps {
                script {
                    // Your Docker commands here
                    sh 'docker build -t your_image_name .'
                    sh 'docker push your_image_name'
                }
            }
        }
    }
}
