pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Hello World'
        echo 'Multiline shell steps works too'
        sh 'ls -lah'
      }
    }

    stage('Lint HTML') {
      steps {
        sh 'tidy -q -e *.html'
      }
    }

    stage('Upload to AWS') {
      steps {
        withAWS(region: 'us-east-2', credentials: 'jenkinsyed')
      }
    }

  }
}