pipeline {
    agent {
        docker {
            image 'alpine:15'
            args '-v /var/run/docker.sock'
        }
    }

    stages {
        stage('Build') {
            steps {
                script {
                    dockerapp = docker.build(registry, "react-app", '-f /src/Dockerfile ./src')
                }
            }
        }
    }
}
