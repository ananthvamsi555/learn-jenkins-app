pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    docker.image('node:18-alpine').inside('-v C:/ProgramData/Jenkins/.jenkins/workspace/Angular_Udemy:/workspace') {
                        bat 'echo "Running node build..."'
                        bat 'npm run build'
                    }
                }
            }
        }
    }
}
