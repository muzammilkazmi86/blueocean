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

        stage('error') {
          steps {
            writeFile(text: '<!doctype html>     <html>       <head>         <title>Static HTML Site</title>       </head>       <body>         <p>This is the first paragraph in a simple Static HTML site. There is no <strong>CSS</strong> or <strong>JavaScript</script>.</p>       </body>     </html>', encoding: 'html', file: 'Index')
            sh 'tidy -q -e *.html'
          }
        }

      }
    }

  }
}