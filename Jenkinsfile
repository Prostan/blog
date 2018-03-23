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
        echo 'mock - It allows you to replace parts of your system under test with mock objects and make assertions about how they have been used.'
        echo 'Hypothesis - library which lets you write tests that are parametrized by a source of examples. It then generates simple and comprehensible examples that make your tests fail, letting you find more bugs with less work.'
      }
    }
    stage('Front-end') {
      steps {
        sh 'echo React tests'
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo Deploy BE Code'
        sh 'echo Deploy FE code'
        sh 'echo Deploy DB code'
      }
    }
    stage('End to End Tests') {
      steps {
        sh 'echo End To End test'
      }
    }
  }
}