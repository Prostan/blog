pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh 'echo build'
          }
        }
        stage('Static Analysis') {
          steps {
            sh 'echo Pylint'
          }
        }
      }
    }
    stage('Back-end') {
      steps {
        sh 'echo uint-tests'
        sh 'echo Data integrity test'
      }
    }
    stage('Front-end') {
      steps {
        sh 'echo React tests'
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo Deploy'
      }
    }
    stage('End to End Tests') {
      steps {
        sh 'echo End To End test'
      }
    }
  }
}