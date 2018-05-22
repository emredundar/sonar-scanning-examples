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
        sh '''



/opt/maven/apache-maven-3.5.3/bin/mvn -version'''
      }
    }
    stage('build') {
      steps {
        sh '''cd sonarqube-scanner-maven /
/opt/maven/apache-maven-3.5.3/bin/mvn clean install sonar:sonar -Dsonar.login=c83855c2be5760fd53f53faf1d2f26a914fb6d23'''
      }
    }
  }
  environment {
    dev = '1'
  }
}