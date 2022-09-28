pipeline {
    agent any
    tools {
        dockerTool 'docker'
    }
    stages {
        stage('Docker Build') {
            steps {
                script {
                    sh 'docker --version'
                }
                
            }
        }
    }
}
