pipeline {
    agent any
    tools {
        dockerTool 'docker'
    }
    stages {
        stage('Docker Build') {
            steps {
                script {
                    sh 'docker build -t petclinic .'
                    sh 'docker images'
                }
            }
        }
        stage ('list images') {
            steps {
                script {
                    sh 'docker images'
                }
            }
        }                
    }
}
