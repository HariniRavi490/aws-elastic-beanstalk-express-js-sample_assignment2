pipeline {
  agent {
    docker { image 'node:16-alpine' }
  }
  stages {
    stage('Checkout') {
      steps {
        checkout scm // This step is for checking out your source code
      }
    }
    stage('Build') {
      steps {
        sh 'npm install --save'
      }
    }
    stage('Test') {
      steps {
        sh 'node --version'
      }
    }
  }
}
