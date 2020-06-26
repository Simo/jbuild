pipeline {
  agent any
  stages {
    stage('compile') {
      parallel {
        stage('compile') {
          steps {
            sh './mvnw compile'
          }
        }

        stage('test') {
          steps {
            sh './mvnw test'
          }
        }

      }
    }

    stage('package') {
      steps {
        sh './mvnw -Pprod clean package'
      }
    }

  }
}