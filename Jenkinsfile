pipeline {
    agent {
        docker {
            args -v '/var/run/docker.sock'
        }
    }

    stages {
        stage('Build') {
            steps {
                script {
                    sh "docker build -t react-app:latest -f /src/Dockerfile ."
                }
            }
        }
    }
}
