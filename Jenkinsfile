pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git(url: 'https://github.com/ielb/nuxt-app', branch: 'master')
      }
    }

    stage('error') {
      steps {
        sh 'npm i && npm run build'
      }
    }

  }
}