pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('svn') {
          steps {
            sh '''/home/enomix/flare/flare-py-1.1/flare_bin/git.sh
/home/enomix/flare/flare-py-1.1/flare_bin/run.sh build svn'''
          }
        }
        stage('mavan') {
          steps {
            sh '/home/enomix/flare/flare-py-1.1/flare_bin/run.sh build maven'
          }
        }
        stage('setup') {
          steps {
            sh '/home/enomix/flare/flare-py-1.1/flare_bin/run.sh build setup'
          }
        }
        stage('clean') {
          steps {
            sh '/home/enomix/flare/flare-py-1.1/flare_bin/run.sh clean'
          }
        }
        stage('run') {
          steps {
            sh '/home/enomix/flare/flare-py-1.1/flare_bin/run.sh build run'
          }
        }
      }
    }
    stage('Deploy') {
      parallel {
        stage('ready') {
          steps {
            sh '/home/enomix/flare/flare-py-1.1/flare_bin/run.sh deploy ready'
          }
        }
        stage('eer') {
          steps {
            sh '/home/enomix/flare/flare-py-1.1/flare_bin/run.sh deploy eer'
          }
        }
        stage('gatling') {
          steps {
            sh '/home/enomix/flare/flare-py-1.1/flare_bin/run.sh deploy gatling'
          }
        }
      }
    }
    stage('Test') {
      parallel {
        stage('ready') {
          steps {
            sh '/home/enomix/flare/flare-py-1.1/flare_bin/run.sh test ready'
          }
        }
        stage('talk') {
          steps {
            sh '/home/enomix/flare/flare-py-1.1/flare_bin/run.sh test talk'
          }
        }
        stage('scenario') {
          steps {
            sh '/home/enomix/flare/flare-py-1.1/flare_bin/run.sh test scenario'
          }
        }
      }
    }
  }
}