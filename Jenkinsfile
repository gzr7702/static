pipeline {
  agent any
  stages {
    stage('Upload to AWS') {
      steps {
        sh 'echo "Hello World"'
        sh '''
          echo "Multinline shell steps works too"
          ls -lsh
          '''
       }
    }
  }
}
