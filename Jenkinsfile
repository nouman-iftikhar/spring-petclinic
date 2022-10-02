pipeline {
    agent any
    stages {
        stage ('Run docker image') {
            steps {
                script {
                    sh 'docker images'
                    sh 'docker stop petclinic'
                    sh '''if [ "$?" == "1" ]; then
                            continue 
                          fi'''
                    sh 'docker rm petclinic'
                    sh "docker run -d --name petclinic -p 8083:8080 rcartifacoty.jfrog.io/petclinic-docker-local/petclinic:${BUILD_NUMBER}"
                }
            }
        }  
    //     stage('Docker Build') {
    //         steps {
    //             script {
    //                 sh 'docker build -t petclinic:latest .'
    //                 sh "docker tag petclinic:latest rcartifacoty.jfrog.io/petclinic-docker-local/petclinic:${BUILD_NUMBER}"
    //                 sh 'docker images'
    //             }
    //         }
    //     }
    //     stage ('Push image to Artifactory') { // take that image and push to artifactory
    //     steps {
    //         rtDockerPush(
    //             serverId: "jfrog",
    //             image: "rcartifacoty.jfrog.io/petclinic-docker-local/petclinic:${BUILD_NUMBER}",
    //             targetRepo: 'petclinic-docker-local',
    //             properties: 'project-name=petclinic;status=stable'
    //         )
    //     }
    // }
    //     stage ('Pull image from Artifactory') { // take that image and push to artifactory
    //     steps {
    //         rtDockerPull(
    //             serverId: "jfrog",
    //             image: "rcartifacoty.jfrog.io/petclinic-docker-local/petclinic:${BUILD_NUMBER}",
    //             sourceRepo: 'petclinic-docker-local'
    //         )
    //     }
    // }
    //     stage ('Run docker image') {
    //         steps {
    //             script {
    //                 sh 'docker images'
    //                 sh 'docker stop petclinic'
    //                 sh 'if [ "$?" == "1" ]; then
    //                     continue
    //                     fi'
    //                 sh 'docker rm petclinic'
    //                 sh "docker run -d --name petclinic -p 8083:8080 rcartifacoty.jfrog.io/petclinic-docker-local/petclinic:${BUILD_NUMBER}"
    //             }
    //         }
    //     }                 
    }
}
