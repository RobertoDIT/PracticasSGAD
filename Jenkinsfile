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
          deploy adapters: [tomcat7(path: '', url: 'http://localhost:8080')], contextPath: 'JenkinsJSF', war: '**/*.war'
      }
    }    
  }
}
