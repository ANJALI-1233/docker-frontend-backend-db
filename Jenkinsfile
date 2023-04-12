pipeline {
  agent any
  stages {
    stage('checkout code') {
      steps {
        git(url: 'https://github.com/ANJALI-1233/docker-frontend-backend-db', branch: 'master')
      }
    }

    stage('log') {
      parallel {
        stage('log') {
          steps {
            sh 'ls -la'
          }
        }

        stage('frontend unit test') {
          steps {
            sh 'cd ocker-frontend-backend-db_master && npm i && npm run build'
          }
        }

      }
    }

  }
}