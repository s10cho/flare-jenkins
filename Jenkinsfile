pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''/home/enomix/flare/flare-py-1.1/flare_bin/git.sh
/home/enomix/flare/flare-py-1.1/flare_bin/run.sh build'''
      }
    }
    stage('Deploy') {
      steps {
        sh '/home/enomix/flare/flare-py-1.1/flare_bin/run.sh deploy'
      }
    }
  }
}