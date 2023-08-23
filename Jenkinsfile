pipeline {
    agent any 

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
