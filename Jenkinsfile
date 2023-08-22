pipeline {
    agent any

    stages {
        stage ('Build') {
            steps {
                script {
                    dockerapp = docker.build("react-app", '-f ./src/Dockerfile', './src')
                }
            }
        }
    }
}