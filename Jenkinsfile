pipeline {
  agent any
  stages {
    stage('checkout code') {
      steps {
        git(url: 'https://github.com/ANJALI-1233/docker-frontend-backend-db', branch: 'master')
      }
    }

    stage('log') {
      steps {
        bat 'dir'
      }
    }

    stage('build') {
      steps {
        bat 'docker-compose up'
      }
    }

  }
}
