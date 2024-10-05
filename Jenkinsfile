pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    docker.image('mcr.microsoft.com/windows/servercore:ltsc2019').inside('-v C:/ProgramData/Jenkins/.jenkins/workspace/Angular_Udemy:/workspace') {
                        // Now using bat for Windows-based container
                        bat 'echo "Running node build..."'
                        bat 'npm run build'
                    }
                }
            }
        }
    }
}
