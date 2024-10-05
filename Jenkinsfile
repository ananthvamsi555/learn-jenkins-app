pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    docker.image('maven:3.3.3').inside('-v /c/ProgramData/Jenkins/.jenkins/workspace/Angular_Udemy:/workspace') {
                        sh 'echo "Running maven build..."'
                        sh 'mvn clean install'
                    }
                }
            }
        }
    }
}
