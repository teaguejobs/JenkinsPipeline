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
            echo 'Get the DriverPath$"chromedriverpath"'
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
         when {
          Branch "master"
         }
        stage('Deploy') {
          steps {
            echo 'Deploying The app in a Server'
          }
        }

        stage('error') {
          steps {
            archiveArtifacts 'logtestfile.txt'
          }
        }

      }
    }

  }
  environment {
    chromedriverpath = '"c:\\chrome\\path\\driver"'
  }
}