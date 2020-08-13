pipeline {
  agent any

  tools {nodejs "node"}

  stages {
    stage('checkout') {
      steps {
//        checkout scm
        sh "git checkout ${BRANCH_NAME}"
        sh "git status"
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
            git config --global user.email "maxim.d.672@gmail.com"
            git config --global user.name "Max"
           npm run release
           git pull
           git status
           git log -n 10 --pretty=format:"%h %s" --graph

        """
      }
    }
    stage('cat ch') {
      steps {
        sh 'cat ./CHANGELOG.md'
      }
    }
//    git push --follow-tags origin ${BRANCH_NAME}
  }
}
