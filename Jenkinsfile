pipeline {
  agent any
  tools {nodejs "nodejs"}
    stage('Test') {
      parallel {
        stage('Static code analysis') {
            steps { sh 'npm run-script lint' }
        }
        stage('Unit tests') {
            steps { sh 'npm run-script test' }
        }
      }
    }
 
    stage('Build') {
      steps { sh 'npm run-script build' }
    }
  }