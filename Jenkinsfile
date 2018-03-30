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
    stage('Back-End Tests') {
      steps {
        sh 'echo uint-tests'
        sh 'echo Data integrity test'
        echo 'mock - It allows you to replace parts of your system under test with mock objects and make assertions about how they have been used.'
        echo 'Hypothesis - library which lets you write tests that are parametrized by a source of examples. It then generates simple and comprehensible examples that make your tests fail, letting you find more bugs with less work.'
      }
    }
    stage('Front-End Tests') {
      steps {
        sh 'echo React tests'
      }
    }
    stage('Stage Deploy') {
      steps {
        sh 'echo Deploy BE Code'
        sh 'echo Deploy FE code'
        sh 'echo Deploy DB code'
      }
    }
    stage('End to End Tests') {
      parallel {
        stage('End to End Tests') {
          steps {
            sh 'echo End To End test'
          }
        }
        stage('Performance Tests') {
          steps {
            sh 'echo Gatling or k6'
          }
        }
      }
    }
    stage('Prod Manual Deploy') {
      parallel {
        stage('Prod Manual Deploy') {
          steps {
            sh 'echo Manual deploy'
          }
        }
        stage('some stage') {
          steps {
            sleep 1
          }
        }
      }
    }
  }
}