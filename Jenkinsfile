pipeline {
  agent any
  stages {
    stage('Get sources') {
      steps {
        git(url: 'git@github.com:eransagi1/cicdcource.git', branch: 'master')
      }
    }
    stage('Install') {
      steps {
        sh 'npm install'
      }
    }
    stage('Test') {
      steps {
        sh 'npm test'
      }
    }
    stage('Build') {
      steps {
        sh 'npm run build'
      }
    }
    stage('Archive') {
      steps {
        archiveArtifacts '*.zip'
      }
    }
  }
}