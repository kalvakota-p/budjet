pipeline {
  agent any
  stage('Checkout SCM') {
    git branch: 'budjetMain', url: 'git@github.com:kalvakota-p/budjet.git'
  }
  stages {
    stage('Install node modules') {
      sh 'npm install' 
    }
 
    stage('Test') {
      sh 'npm run test-headless'
    }
 
    stage('Build') {
      sh 'npm run build'
    }
  }
}