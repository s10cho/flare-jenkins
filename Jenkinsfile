pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''cd /home/enomix/flare/flare-py-1.1
python3 flare.py build docker'''
      }
    }
    stage('Deploy') {
      steps {
        sh '''cd /home/enomix/flare/flare-py-1.1
sleep 5'''
      }
    }
  }
}