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
        stage('Docker Run') {
            steps {
                script {
                    sh 'docker images'
                    sh 'docker run -d -p 8081:8080 petclinic'
                }
            }
        }                 
    }
}
