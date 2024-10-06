pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    docker.image('node:18-alpine').inside("-v C:/ProgramData/Jenkins/.jenkins/workspace/Angular_Udemy@2:/workspace") {
                    bat 'npm install'
                      }
                    }
                }
            }
        }
    }
}
