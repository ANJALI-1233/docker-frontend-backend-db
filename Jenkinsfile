pipeline {
  agent any
  stages {
    stage('checkout code') {
      steps {
        git(url: 'https://github.com/ANJALI-1233/docker-frontend-backend-db', branch: 'master', credentialsId: 'ANJALI-1233/malviya@98')
      }
    }

    stage('log') {
      parallel {
        stage('log') {
          steps {
            bat 'dir'
          }
        }

        stage('frontend unit test') {
          steps {
            bat 'npm i && npm run build'
          }
        }

      }
    }

  }
}