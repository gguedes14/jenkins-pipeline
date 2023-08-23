pipeline {
    agent any 

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
