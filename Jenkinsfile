pipeline {
    agent any

    environment {
        DOCKER_BUILDKIT = '1'
    }

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    sh 'docker build -t react-app:latest -f ./src/Dockerfile ./src'
                }
            }
        }
    }
}
