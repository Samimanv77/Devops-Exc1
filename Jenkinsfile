pipeline {
  agent {
    docker {
      image 'node:8-alpine'
      args ' -p 3000:3000'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }
    stage('test') {
      steps {
        sh 'npm test'
      }
    }
    stage('deploy') {
      steps {
        sh 'npm start'
      }
    }
  }
}