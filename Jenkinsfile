pipeline {
  agent any
  stages {
    stage('Lint') {
      agent any
      steps {
        sh 'tidy -q -e *.html'
      }
    }

  }
}