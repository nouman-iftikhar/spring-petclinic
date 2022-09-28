pipeline {
    agent any
    stages {
        stage('Docker Build') {
            steps {
                script {
                    def newApp = docker.build "pet:${env.BUILD_TAG}"
                    sh 'docker images'
                }
                
            }
        }
    }
}
