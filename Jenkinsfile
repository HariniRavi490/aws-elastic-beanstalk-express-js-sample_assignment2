pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Pull the Node 16 Docker image and run npm install
                script {
                    docker.image('node:16').run('npm install --save')
                }
            }
        }
    }
}
