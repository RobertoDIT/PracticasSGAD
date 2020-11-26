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
          deploy adapters: [tomcat7(credentialsId: '10f14312-cd85-44af-ab91-243eb29d6faf', path: '', url: 'http://localhost:8081')], contextPath: 'JenkinsJSF', war: '**/*.war'
      }
    }    
  }
}
