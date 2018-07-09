pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '/home/enomix/flare/flare-py-1.1/flare_bin/run.sh build'
      }
    }
    stage('Deploy') {
      steps {
        sh '/home/enomix/flare/flare-py-1.1/flare_bin/run.sh deploy'
      }
    }
    stage('Test') {
      steps {
        sh '/home/enomix/flare/flare-py-1.1/flare_bin/run.sh test'
      }
    }
    stage('Report') {
      steps {
        sh 'sleep 1'
      }
    }
  }
}