pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh 'npm install'
          }
        }
        stage('Git') {
          steps {
            git(url: 'https://github.com/vckbansod12/node_multibranch.git', branch: 'master')
          }
        }
      }
    }
    stage('Test') {
      steps {
        sh '''chmod +x test1.sh
'''
      }
    }
  }
  environment {
    CI = 'true'
  }
}