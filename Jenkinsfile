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
        sh 'printenv'
        sh 'source /etc/profile.d/maven.sh'
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