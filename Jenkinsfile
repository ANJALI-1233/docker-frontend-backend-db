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
            sh 'cd  && cd /var/lib/jenkins/workspace/ocker-frontend-backend-db_master/frontend && npm i && npm run build'
          }
        }

      }
    }

  }
}