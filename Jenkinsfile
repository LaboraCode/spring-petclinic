pipeline {
  agent any
  stages {
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
  -Dsonar.login=51fd982bf91450ebd501ec63ebecd360d8890758'''
      }
    }

  }
}