pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    // Use a Windows Docker image instead of node:18-alpine
                    docker.image('mcr.microsoft.com/windows/servercore:ltsc2019').inside('-v C:/ProgramData/Jenkins/.jenkins/workspace/Angular_Udemy:/workspace') {
                        // Now you can use bat commands as the container is running Windows
                        bat 'echo "Running node build..."'
                        bat 'npm run build'
                    }
                }
            }
        }
    }
}
