pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    docker.image('node:18-alpine').inside {
                        // Run npm install inside the container
                        bat 'npm install'
                    }
                }
            }
        }
    }
}
