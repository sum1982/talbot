pipeline {
  agent any
  stages {
    stage('Check for pom') {
      steps {
        fileExists 'pom.xml'
      }
    }

  }
}