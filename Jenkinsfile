pipeline {
  agent any
  stages {
    stage('Upload to AWS.') {
      steps {
        withAWS(credentials: 'aws-credentials', region: 'us-east-2') {
        sh 'echo "Hello World"'
        sh '''
          echo "Multiline shell steps works too"
          ls -lah
         '''
        }
         }
        }
      }
   }
       
