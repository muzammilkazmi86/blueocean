pipeline {
  agent any
  libraries {
    lib('GroovyLib')
  }
  stages {
    stage('print message') {
      steps {
        echo "Hello ${MY_NAME} ${params.Name}!"
      }
    }
    stage('Get Kernel') {
      steps {
        bat 'ipconfig'
      }
    }
     stage('Shared Lib') {
         steps {
             helloWorld("Jenkins")
         }
      }
    stage('Deploy') {
      input {
        message 'Which Version?'
        id 'Deploy'
        parameters {
          choice(name: 'APP_VERSION', choices: '''v1.1
v1.2
v1.3''', description: 'What to deploy?')
        }
      }
      steps {
        echo "Deploying ${APP_VERSION}."
      }
    }
  }
  environment {
    MY_NAME = 'Sai'
  }
  post {
    aborted {
      echo 'Why didn\'t you push my button?'
      
    }
    
  }
  parameters {
    string(name: 'Name', defaultValue: 'whoever you are', description: 'Who should I say hi to?')
  }
}
