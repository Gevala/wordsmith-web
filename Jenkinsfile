pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building the wordsmith API application...'
        // Example build command
          sh '''
               go mod init wordsmith
               go mod tidy
               go build 
            '''
      }
    }
    stage('Push')  {
      steps {
        echo 'pushing image to dockerhub'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying the application'
   //     sh 'docker run -d -p 80:80 pheyishayor001/wordsmithwebimage'
      }
    }
  }
}
