pipeline {
  agent any
  stages {
    stage('compilar') {
      steps {
        withMaven(maven: 'Maven-1') {
          bat 'mvn clean install -DskipTests=true'
        }
      }
    }
    stage('desplegar') {
      steps {
          deploy adapters: [tomcat7(path: '', url: 'http://localhost:8081')], contextPath: 'C:\Windows\System32\config\systemprofile\AppData\Local\Jenkins\.jenkins\workspace\PracticasSGAD_master', war: 'JenkinsJSF-0.0.1-SNAPSHOT.war'
      }
    }    
  }
}
