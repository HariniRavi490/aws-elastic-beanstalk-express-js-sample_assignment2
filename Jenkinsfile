pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    docker.image('node:16-alpine').inside {
                        sh 'npm install --save'
                    }
                }
            }
}
    }
}
