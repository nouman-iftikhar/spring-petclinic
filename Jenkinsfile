pipeline {
    agent any
    tools {
        dockerTool 'docker'
    }
    stages {
        // stage('Docker Build') {
        //     steps {
        //         script {
        //             sh 'docker build -t petclinic .'
        //             sh 'docker images'
        //         }
        //     }
        // }
        stage ('list images') {
            steps {
                script {
                    sh 'systemctl daemon-reload'
                    sh 'systemctl restart docker'
                    sh 'sudo service docker status'
                }
            }
        }                
    }
}
