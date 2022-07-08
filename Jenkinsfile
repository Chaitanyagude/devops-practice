pipeline {
  agent any
  stages {
    stage('Sample') {
      steps {
        sh "echo Hello..."
      }
    }
  }
  post {
    success {
      echo "This is success block'
    }
    failure {
      echo "This is failure block"
    }
  }
}
