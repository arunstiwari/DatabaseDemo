pipeline {
  agent any
  stages {
    stage('Initialize') {
      steps {
        echo 'Starting the database deployment'
      }
    }
    stage('Deploy') {
      steps {
        sh './libexec/flyway clean'
      }
    }
  }
}