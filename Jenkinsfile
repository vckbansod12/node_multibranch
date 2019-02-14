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
        stage('Trigger Build on Every Commit') {
          steps {
            git(poll: true, credentialsId: 'c8f540b0-cdd8-44be-99a1-996367825fc2', url: 'https://github.com/vckbansod12/node_multibranch.git', branch: 'master', changelog: true)
          }
        }
      }
    }
    stage('Test') {
      steps {
        sh '''chmod +x test.sh
'''
      }
    }
  }
  environment {
    CI = 'true'
  }
}