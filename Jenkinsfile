pipeline {
  agent any

  stages {

    stage('Lint HTML') {
      steps {
        sh 'tidy -q -e *.html'
      }
    }

    stage('Upload to AWS') {
      steps {
        sh 'echo "Uploading code from S3"'
        withAWS(region:'us-east-2', credentials:'jenkins') {
          s3Upload(file:'index.html', bucket:'gzr7702jenkinsbucket')
        }
      }
    }
  }
}
