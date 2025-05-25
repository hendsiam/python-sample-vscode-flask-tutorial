pipeline {
  agent any
  stages {
    stage('Build Docker Image') {
      steps {
        sh 'docker build -t hendsiam/jenkins:v8 .'
      }
    
    stage('Push Docker Image') {
      steps {
        sh 'docker push hendsiam/jenkins:v8'
      }
    }
  }
}
