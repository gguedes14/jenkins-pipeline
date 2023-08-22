pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    def dockerapp = docker.build("react-app:latest", "-f ./src/Dockerfile", "./src")
                }
            }
        }
    }
}
