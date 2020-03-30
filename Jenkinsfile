pipeline {
  agent any
  stages {
    state('Build') {
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
