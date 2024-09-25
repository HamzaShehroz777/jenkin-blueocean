pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''pwd
date'''
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'Test Step'
          }
        }

        stage('Test parallel') {
          steps {
            echo 'Parallel pipeline'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'deploy'
        sh 'sleep 5'
      }
    }

  }
}