pipeline {
  agent any
  stages {
    stage('Install Dependencies') {
      steps {
        sh 'npm install'
      }
    }
    stage('Build') {
      steps {
        sh 'npm run build'
      }
    }
    stage('Test') {
      steps {
        sh 'npm test'
      }
    }
    stage('Docker Build') {
      steps {
        sh 'docker build -t myapp .'
      }
    }
    stage('Docker Push') {
      steps {
        sh 'docker push myrepo/myapp'
      }
    }
  }
}
