pipeline {
  agent any
  stages {
    stage('test') {
      steps {
        sh './mvnw test'
      }
    }

    stage('package') {
      steps {
        sh './mvnw -Pprod clean package -DskipTests'
      }
    }
      
    post {
        always {
            archiveArtifacts artifacts: 'target/*.jar', fingerprint: true
            junit 'target/reports/**/*.xml'
        }
    }

  }
}
