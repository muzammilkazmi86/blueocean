pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'Hello World'
            echo 'Multiline shell steps works too'
            sh 'ls -lah'
          }
        }

        stage('Lint HTML') {
          agent any
          steps {
            sh '''tidy -q -e *.html
'''
          }
        }

      }
    }

  }
}