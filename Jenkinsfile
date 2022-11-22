pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'Building the .Net core Application'
          }
        }

        stage('Test') {
          steps {
            echo 'Testing The Application'
            echo 'Get theDriverPath$"chromedriverpath"'
          }
        }

        stage('error') {
          steps {
            writeFile(file: 'logtestfile.txt', text: 'this is an automation ')
          }
        }

      }
    }

    stage('Deploy') {
      parallel {
        stage('Deploy') {
          steps {
            echo 'Deploying The app in a Server'
          }
        }

        stage('') {
          steps {
            archiveArtifacts 'testlogfile.txt'
          }
        }

      }
    }

  }
  environment {
    chromedriverpath = '"c:\\chrome\\path\\driver"'
  }
}