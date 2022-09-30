pipeline {
    agent any
    stages {
        stage('Docker Build') {
            steps {
                script {
                    sh 'docker build -t petclinic:latest .'
                    sh 'docker tag petclinic:latest rcartifacoty.jfrog.io/petclinic-docker-local/petclinic:latest'
                    sh 'docker images'
                }
            }
        }
        // stage('Docker Run') {
        //     steps {
        //         script {
        //             sh 'docker run -d -p 8081:8080 petclinic'
        //         }
        //     }
        // }
        stage ('Push image to Artifactory') { // take that image and push to artifactory
        steps {
            rtDockerPush(
                serverId: "jfrog",
                image: "rcartifacoty.jfrog.io/petclinic-docker-local/petclinic:latest",
                targetRepo: 'petclinic-docker-local', // where to copy to (from docker-virtual)
                properties: 'project-name=docker1;status=stable'
            )
        }
    }                 
    }
}
