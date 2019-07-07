pipeline {
  agent any
  stages {
    stage('Get sources') {
      steps {
        git(url: 'https://github.com/eransagi1/cicdcource.git', branch: 'master')
      }
    }
    stage('Install') {
      steps {
        sh 'echo npm install'
      }
    }
    stage('Test') {
      steps {
        sh 'echo npm test'
      }
    }
    stage('Build') {
      steps {
        sh 'echo npm run build'
      }
    }
  }
}