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
            echo "Get the DriverPath$(chromedriverpath)"
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