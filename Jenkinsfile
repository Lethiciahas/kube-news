pipeline {
    agente any

    stages {

        stage ('Build Docker Image') {
            steps {
                script {
                    dockerapp = docker.build("lethiciahas/kube-news:${env.BUILD_ID}", '-f /home/lethicia/jornada_devops/kube-news/src/Dockerfile ./src')

                }
            }
        }
    }
}