pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'ls -a'
        sh 'sh ./gradle build'
      }
    }

    stage('sonarqube') {
      steps {
        sh '''sh ./gradlew sonarqube \\
  -Dsonar.projectKey=ingSoft \\
  -Dsonar.host.url=http://localhost:9000 \\
  -Dsonar.login=cbdb6700d95f22dd8a62dc9316016d6e656ec5e6'''
      }
    }

  }
}