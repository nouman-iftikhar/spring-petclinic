pipeline {
    agent any
    tools {
        dockerTool 'docker'
    }
    stages {
        stage('Docker Build') {
            steps {
                script {
                    sh 'docker build .'
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
