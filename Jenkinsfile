pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build completed'
        retry(count: 3) {
        echo 'Build completed'
        }

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
            input(message: 'are you sure to Deploy', ok: 'Yes, I\'m sure')
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

    stage('Notify') {
      steps {
        echo 'Deploy Completed'
      }
    }

  }
}
