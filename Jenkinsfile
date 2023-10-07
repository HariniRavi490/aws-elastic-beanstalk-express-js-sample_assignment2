pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Pull the Node 16 Docker image
                    docker.image('node:16').inside {
                        // Run npm install --save
                        sh 'npm install --save'
                    }
                }
            }
        }
    }
}
