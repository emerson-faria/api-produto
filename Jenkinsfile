pipeline {
    agent any

    stages {
        stage ('Build Image') {
            steps {
                script { 
                   dockerapp = docker.build("emerson-faria/api-produto:${env.BUILD_ID}", '-f /home/vagrant/api-produto/src/Dockerfile ./src') 
                }
            }
        }

       # stage ('Push Image') {
            steps {
                script {
                    docker.withRegistry('https://registry.hub.docker.com', 'dockerhub') {
                        bat "docker push emerson-faria/api-produto:${env.BUILD_ID}"
                        bat "docker push emerson-faria/api-produto:latest"
                    }
                }
            }
        }
    }
}
