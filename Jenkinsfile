pipeline {
    agent {
            docker {
            image 'node:14'
            args '-v /var/run/docker.sock:/var/run/docker.sock'
        }
    }
    }

    stages {
        stage('Build') {
            steps {
                script {
                    dockerapp = docker.build("react-app:latest", "-f ./src/Dockerfile .")
                }
            }
        }
    }
}
