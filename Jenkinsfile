pipeline {
    agent {
        docker {
            image 'react-app:latest'
            args '-v /var/run/docker.sock:/var/run/docker.sock'
        }
    }

    stages {
        stage('Build') {
            steps {
                script {
                    dockerapp = docker.build("react-app:latest", "-f ./src/Dockerfile ./src")
                }
            }
        }
    }
}
