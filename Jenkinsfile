pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''cd /home/enomix/flare/flare-py-1.1/flare_module
python3 flare.py build'''
      }
    }
    stage('Deploy') {
      steps {
        sh '''cd /home/enomix/flare/flare-py-1.1/flare_module
python3 flare.py deploy'''
      }
    }
  }
}