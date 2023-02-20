pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'g++ main/main.cpp -o main'
        build job: 'PES1UG20CS353', wait: false
        echo 'Build Stage successful'
        }
    }
    stage('Test') {
      steps {
        sh 'cat error.cpp'
        echo 'Test Stage successful'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deployment successful'
       }
    }
  }
  post {
    failure {
      echo 'Pipeline failed'
    }
  }
}
