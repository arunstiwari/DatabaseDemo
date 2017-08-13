pipeline {
  agent any
  stages {
    stage('Initialize') {
      steps {
        echo 'Starting the database deployment'
      }
    }
    stage('Clean') {
      steps {
        sh './libexec/flyway -configFile=./libexec/conf/ci.conf clean'
      }
    }
    stage('Deploy') {
      steps {
        sh './libexec/flyway -configFile=./libexec/conf/ci.conf migrate'
      }
    }
  }
}