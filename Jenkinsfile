pipeline {
    agent any
    stages {
        stage('Docker Build') {
            steps {
                def newApp = docker.build "pet:${env.BUILD_TAG}"
                sh 'docker images'
            }
        }
    }
}
