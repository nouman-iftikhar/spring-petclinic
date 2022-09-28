pipeline {
    agent any
    // tools {
    //     dockerTool 'docker'
    // }
    stages {
        stage('Docker Build') {
            steps {
                script {
                    sh 'docker build -t petclinic .'
                    sh 'docker images'
                }
            }
        }              
    }
}
