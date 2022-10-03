pipeline {
    agent any

    stages {
        stage ('Build Image') {
            steps {
                script { 
                   dockerapp = docker.build("mersonmoraes/api-produto", '-f .src/Dockerfile ./src') 
                }
            }
        }
    }
}