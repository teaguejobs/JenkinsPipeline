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

        stage('') {
          steps {
            writeFile(file: 'logtestfile.txt', text: 'this is an automation ')
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying The app in a Server'
      }
    }

  }
  environment {
    chromedriverpath = '"c:\\chrome\\path\\driver"'
  }
}