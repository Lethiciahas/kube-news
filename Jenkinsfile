pipeline {
    agent any

    stages {

        stage ('Build Docker Image') {
            steps {
                script {
                    dockerapp = docker.build("lethiciahas/kube-news:${env.BUILD_ID}", '-f ./src/Dockerfile ./src')

                }
            }
        }

        stage ('Push Docker Image') {
            steps {
                script {
                    withDockerRegistry([credentialsId: 'dockerhub', url:'https://registry.hub.docker.com/')
                    dockerapp.push()
                }
            }
        }
    }
}