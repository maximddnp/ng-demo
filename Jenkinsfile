pipeline {
  agent any

  tools {nodejs "node"}

  stages {
    stage('checkout') {
      steps {
        sh "git checkout ${BRANCH_NAME}"
      }
    }
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }
    stage('Stage release') {
      steps {
        sh """
            git config --global user.email "maximapr1@gmail.com"
            git config --global user.name "Max"
           npm run release
           git status
           git push --follow-tags origin HEAD
        """
      }
    }
  }
}
