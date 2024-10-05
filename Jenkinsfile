pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    docker.image('maven:3.3.3').inside('-v /c/ProgramData/Jenkins/.jenkins/workspace/Angular_Udemy:/workspace') {
                        bat 'echo "Running maven build..."'
                    }
                }
            }
        }
    }
}
