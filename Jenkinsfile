pipeline {
  agent any
  stages {
    stage('Check for pom') {
      parallel {
        stage('Check for pom') {
          steps {
            fileExists 'pom.xml'
          }
        }

        stage('') {
          steps {
            sh '''mvn --version
git --version
java -version'''
          }
        }

      }
    }

    stage('Build with Maven') {
      steps {
        sh 'mvn compile test package'
      }
    }

    stage('Post Build Steps') {
      steps {
        writeFile(file: 'status.txt', text: 'Hey let\'s see if it works')
      }
    }

  }
}