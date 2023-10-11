pipeline {
  agent {
    docker { image 'node:16-alpine' }
  }
  stages {
    stage('Test') {
      steps {
        sh 'node --version'
      }
    }
  }
  stages {
        stage('Build') { 
            steps {
                sh 'npm install' 
            }
        }
    }
}



