pipeline {
  agent any
  stages {
    stage('Upload to AWS.') {
      steps {
        sh 'echo "Hello World"'
        sh '''
          echo "Multiline shell steps works too"
          ls -lah
         '''
         withAWS(credentials: 'aws-credentials', region: 'us-east-2') {
         sh 'echo "hello KB">hello.txt'
                    s3Upload acl: 'Public', bucket: 'jenkinss3udacity', file: 'index.html'
                    sh 'cat index.html'        
         }
        }
      }
   }
       
