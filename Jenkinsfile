pipeline {
  agent {
    docker {
      image 'node:6-alpine'
      args '-p 3000:3000'
    }
  }
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }
    stage('Stage release') {
      steps {
        sh """
           npm run release
        """
      }
    }
    stage('Stage push') {
      steps {
        sh """
           npm run release:tags
        """
      }
    }
  }
}
