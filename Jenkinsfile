pipeline {
  agent any
  stages {
    stage('prep') {
      environment {
        dev = '1'
      }
      steps {
        echo 'ready to start'
        sh '''



/opt/maven/apache-maven-3.5.3/bin/mvn -version / cd sonarqube-scanner-maven'''
      }
    }
    stage('build') {
      steps {
        sh '''
/opt/maven/apache-maven-3.5.3/bin/mvn clean install sonar:sonar -Dsonar.login=c83855c2be5760fd53f53faf1d2f26a914fb6d23 -Dsonar.host.url=http://172.30.227.113:9000'''
      }
    }
  }
}