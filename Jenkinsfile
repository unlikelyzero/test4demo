pipeline {
  agent any
  stages {
    stage('NPM Build') {
      steps {
        sleep 5
      }
    }
    stage('Unit Tests') {
      steps {
        sleep 5
      }
    }
    stage('UI Tests') {
      parallel {
        stage('UI Tests') {
          steps {
            echo 'UI TESTS ARE RUNNING'
          }
        }
        stage('Chrome') {
          steps {
            sleep 3
          }
        }
        stage('Ffox') {
          steps {
            sleep 4
          }
        }
        stage('IE11') {
          steps {
            sleep 6
            sh 'exit 1'
          }
        }
      }
    }
    stage('Reporting') {
      steps {
        echo 'PASS!!!!'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deployed to Prod'
      }
    }
  }
}