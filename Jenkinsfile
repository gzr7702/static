pipeline {
  agent any
  stages {
    stage('Upload to AWS') {
      steps {
        sh 'echo "Uploading code from S3"'
        withAWS(region:'eu-west-1', credentials:'IDofAwsCredentials') {
          s3Upload(file:'index.html, bucket:'gzr7702jenkinsbucket', path:'index.html')
        }
       }
    }
  }
}
