pipeline {
    agente any

    stages {

        stage ('Build Docker Image') {
            steps {
                script {
                    dockerapp = docker.build("lethiciahas/kube-news:${env.BUILD_ID}", '-f ./src/Dockerfile, ./src')

                }
            }
        }
    }
}