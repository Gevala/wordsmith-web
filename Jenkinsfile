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
    stage('Push to nexus')  {
      steps {
        echo 'pushing to nexus'
      }
    }
    
    stage('build in docker')  {
      steps {
        echo 'pushing to nexus'
        sh 'docker build -t wordsmithweb . '
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
