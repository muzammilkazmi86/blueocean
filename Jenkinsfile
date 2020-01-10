pipeline {
  agent any
  stages {
    stage('helloworld') {
      parallel {
        stage('helloworld') {
          steps {
            echo 'Hello World'
          }
        }

        stage('') {
          steps {
            echo 'Multiline shell steps works too'
          }
        }

      }
    }

  }
}