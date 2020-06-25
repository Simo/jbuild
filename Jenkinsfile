pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh './mvnw -Pprod clean verify'
      }
    }

  }
}