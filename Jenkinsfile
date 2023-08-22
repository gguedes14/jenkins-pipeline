pipeline {
    agent any

    stages {
        stage ('Build') {
            steps {
                echo 'Starting Pipeline'
                script {
                    dockerapp = docker.build("react-app", '-f /src/Dockerfile')
                }
            }
        }
    }
}