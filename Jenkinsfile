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
  -Dsonar.login=3aaa41ff57af3b850e403c9cf6d0f32861280a34'''
      }
    }

  }
}