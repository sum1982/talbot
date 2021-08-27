pipeline {
  agent any
  stages {
    stage('Check for pom') {
      steps {
        fileExists 'pom.xml'
      }
    }

    stage('Log Tool Version') {
      steps {
        sh 'mvn -- version'
      }
    }

  }
}