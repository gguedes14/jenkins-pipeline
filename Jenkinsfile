pipeline {
    agent any

    stages {
        stage ('Pre-build') {
            steps {
                echo 'Starting Pipeline'
                script {
                    dockerapp = docker.build("react-app:latest", '-f ./src/Dockerfile ./src')
                }
            }
        }
    }
}