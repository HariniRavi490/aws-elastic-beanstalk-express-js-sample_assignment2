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
        sh 'npm test' // You can run your test suite here
      }
    }
    stage('Lint') {
      steps {
        sh 'npm run lint' // You can add linting tasks here
      }
    }
    stage('Build Docker Image') {
      steps {
        sh 'docker build -t my-node-app .'
      }
    }
    stage('Push Docker Image') {
      steps {
        withCredentials([usernamePassword(credentialsId: 'docker-hub-credentials', usernameVariable: 'DOCKER_HUB_USERNAME', passwordVariable: 'DOCKER_HUB_PASSWORD')]) {
          sh "docker login -u $DOCKER_HUB_USERNAME -p $DOCKER_HUB_PASSWORD"
          sh 'docker push my-node-app'
        }
      }
    }
  }
}
