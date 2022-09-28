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
                    sh 'sudo docker build -t petclinic .'
                    sh 'sudo docker images'
                }
            }
        }
        // stage ('list images') {
        //     steps {
        //         script {
        //             sh 'systemctl status docker'
        //         }
        //     }
        // }                
    }
}
