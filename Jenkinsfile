pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    // Use a Windows Docker image instead of node:18-alpine
                    docker.image('node:18-alpine').inside('-v C:/ProgramData/Jenkins/.jenkins/workspace/Angular_Udemy:/workspace') {
                    reuseNode true    
                        // Now you can use bat commands as the container is running Windows
                        bat 'echo "Running node build..."'
                        bat 'npm run build'
                    }
                }
            }
        }
    }
}
