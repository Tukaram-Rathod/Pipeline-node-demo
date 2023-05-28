pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        sh 'docker build -t tukaramrathod02/deom:v1 .'
      }
    }

    stage('Deploy') {
      steps {
        sh 'kubectl apply -f deployment.yaml'
        sh 'kubectl apply -f service.yaml'
      }
    }
  }
}

