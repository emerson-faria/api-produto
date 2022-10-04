pipeline {
    agent any

    stages {
        stage ('Build Image') {
            steps {
                script { 
                   dockerapp = docker.build("emerson-faria/api-produto", '-f /home/vagrant/api-produto/src/Dockerfile ./src') 
                }
            }
        }
    }
}