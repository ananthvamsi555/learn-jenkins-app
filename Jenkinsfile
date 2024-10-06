pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    // Use the absolute path of Jenkins workspace with Docker
                    def workspacePath = "${env.WORKSPACE}"

                    // Running the node container with the Jenkins workspace mounted as a volume
                    docker.image('node:18-alpine').inside("--mount type=bind,source=${workspacePath},target=/workspace") {
                        // Run the npm install inside the container
                        bat 'npm install'
                    }
                }
            }
        }
    }
}
