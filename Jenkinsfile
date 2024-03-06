pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'g++ main.cpp -o output'
      }
    }
    stage('Test') {
      steps {
        sh './output'
      }
    }
    stage('Deploy') {
      steps {
        sh 'ls non_existing_file.txt'
        echo 'deploy'
      }
    }
  }
  post {
    failure {
      echo 'Pipeline failed'
    }
  }
}
