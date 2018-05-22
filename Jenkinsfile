pipeline {
  agent any
  stages {
    stage('first') {
      environment {
        dev = '1'
      }
      steps {
        echo 'ready to start'
        sh 'pwd'
        sh '''source /etc/profile.d/maven.sh
printenv'''
      }
    }
    stage('build') {
      steps {
        sh 'mvn -version'
      }
    }
  }
  environment {
    dev = '1'
  }
}