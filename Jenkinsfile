pipeline {
    agent any

    stages {
        stage('w/o docker') {
            steps {
                bat 'echo "Without docker"'
            }
        }

        stage('w/ docker') {
            agent {
                docker {
                    image 'node:18-alpine'
                }
            }
            steps {
                bat 'echo "With docker"'
                bat 'npm --version'
            }
        }
    }
}
