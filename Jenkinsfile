pipeline {
  agent none
  stages {
    stage('Build') {
      steps {
        sh '''cd /home/enomix/flare/flare-py-1.1
python3 flare.py build'''
      }
    }
    stage('Deploy') {
      steps {
        sh '''cd /home/enomix/flare/flare-py-1.1
python3 flare.py deploy'''
      }
    }
  }
}