pipeline {
  agent any
  stages {
    stage('Unit Test') { 
      steps {
        sh 'mvn clean'
      }
    }
    stage('Deploy Standalone') { 
      steps {
        echo 'Hello world!' 
      }
    }
    stage('Deploy ARM') { 
       echo 'Hello world!' 
      }
      steps {
        echo 'Hello world!' 
    }
    stage('Deploy CloudHub') { 
      environment {
        ANYPOINT_CREDENTIALS = credentials('anypoint.credentials')
      }
      steps {
        sh 'mvn deploy -P cloudhub -Dmule.version=3.9.0 -Danypoint.username=${ANYPOINT_CREDENTIALS_USR} -Danypoint.password=${ANYPOINT_CREDENTIALS_PSW}' 
      }
    }
  }
}