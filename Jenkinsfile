pipeline {
  agent any

  stages {

    stage('Upload to AWS') {

      steps {
        sh 'echo "Uploading code from S3"'
        withAWS(region:'eu-east-2', credentials:'IDofAwsCredentials') {
          s3Upload(file:'index.html, bucket:'gzr7702jenkinsbucket', path:'/')
        }
      }
    }
  }
}
