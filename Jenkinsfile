pipeline {
  agent any
  stages {
    stage('compilar') {
      steps {
        withMaven(globalMavenSettingsFilePath: 'C:\\Archivos\\Programas\\apache-maven-3.6.3\\conf', jdk: 'C:\\Program Files\\Java\\jdk1.8.0_131', maven: 'C:\\Archivos\\Programas\\apache-maven-3.6.3\\bin', mavenSettingsFilePath: 'C:\\Archivos\\Programas\\apache-maven-3.6.3\\conf') {
          bat 'mvn clean install -D skipTest'
        }

      }
    }

  }
}