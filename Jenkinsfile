@Library("chaitu-libs") _
pipeline {
  agent any

    stages {
      stage('Maven Build') {
        steps {
          sh 'mvn clean package'
      }
    }
    stage('Deploy to Dev Tomcat') {
      steps {
          tomcatDeploy('172.31.40.218','app','tomcat-dev')
      }
    }
  }
  post {
    success {
      archiveArtifacts artifacts: 'target/*.war'
      cleanWs()
    }
  }
}
