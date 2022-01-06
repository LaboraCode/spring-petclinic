pipeline {
  agent any
  stages {
    stage('error') {
      parallel {
        stage('error') {
          steps {
            sh './mvnw package'
          }
        }

        stage('SonarQube') {
          steps {
            sh '''./gradlew sonarqube \\
  -Dsonar.projectKey=LaboraClinic \\
  -Dsonar.host.url=http://localhost \\
  -Dsonar.login=44a2878cb9b0fa5d5a4d9760267ff462bec09e42'''
          }
        }

      }
    }

  }
}