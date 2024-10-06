pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    docker.image('node:18-alpine').inside("-v ${WORKSPACE}:/workspace") {
                        bat 'npm install'
                    }
                }
            }
        }
    }
}
