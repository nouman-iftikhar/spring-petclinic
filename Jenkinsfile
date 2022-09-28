pipeline {
    agent any
    // tools {
    //     dockerTool 'docker'
    // }
    stages {
        stage('Docker Build') {
            steps {
                script {
                    def myEnv = docker.build 'my-environment:snapshot'
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
