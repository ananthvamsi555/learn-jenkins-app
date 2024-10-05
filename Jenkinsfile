pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    docker.image('maven:3.3.3-windows').inside('-v C:/ProgramData/Jenkins/.jenkins/workspace/Angular_Udemy:/workspace') {
                        bat 'echo "Running maven build..."'
                        bat 'mvn clean install'
                    }
                }
            }
        }
    }
}
