pipeline {
    agent any
    stages {
        stage {
            steps {
                def newApp = docker.build "pet:${env.BUILD_TAG}"
                sh 'docker images'
            }
        }
    }
}
