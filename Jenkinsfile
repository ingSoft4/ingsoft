pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'ls'
        sh 'sh ./gradle build'
      }
    }

    stage('sonarqube') {
      steps {
        sh '''sh ./gradlew sonarqube \\
  -Dsonar.projectKey=ingSoft \\
  -Dsonar.host.url=http://192.168.0.12:9000 \\
  -Dsonar.login=0776ec7b9e033b245bf8021bc790d788bdbdc84d'''
      }
    }

  }
}