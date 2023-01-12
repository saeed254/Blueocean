pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build completed'
      }
    }

    stage('Test') {
      parallel {
        stage('Test Stages') {
          steps {
            echo 'Test completed'
          }
        }

        stage('Test1') {
          steps {
            echo 'Test1 completed'
          }
        }

        stage('Test2') {
          steps {
            echo 'Test2 completed'
          }
        }

      }
    }

    stage('Deploy ') {
      parallel {
        stage('Deploy ') {
          steps {
            echo 'Running Deployment '
          }
        }

        stage('Publish') {
          steps {
            echo 'Now is Published'
          }
        }

      }
    }

  }
}