pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git(url: 'https://github.com/ielb/nuxt-app', branch: 'master')
      }
    }

    stage('build') {
      steps {
        sh 'npm i && npm run build'
      }
    }

    stage('Run') {
      steps {
        sh 'pm2 start .output/server/index.mjs --name frontend'
      }
    }

  }
}