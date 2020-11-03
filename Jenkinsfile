pipeline {
    agent any 
    stages {
        stage('Clean package') {
            steps {
       			bat 'mvn -B -U -e -V clean -DskipTests package'
            }
        }
        stage('Deploy Development') {
      environment {
        ENVIRONMENT = 'Sandbox'
        
      }
      	steps {
            bat 'mvn -U -V -e -B -DskipTests deploy -Dusername=rajesh112020 -Dpassword=MUL22soft -Denvironment=Sandbox -Dmule.version=4.3.0 -Dworkers=1 -Dworker.type=Micro -Dapplication.name=rajesh.sfgetrecords  -DmuleDeploy
    
    }}
}