pipeline {
  agent any

  tools {nodejs "node"}

  stages {
    stage('checkout') {
      steps {
//        checkout scm
//        sh "git checkout ${BRANCH_NAME}"
        checkout([$class: 'GitSCM', branches: [[name: '*/master/*']], doGenerateSubmoduleConfigurations: false, extensions: [[$class: 'LocalBranch', localBranch: "**"]], submoduleCfg: []])
        sh "git status"
      }
    }
//    stage('Build') {
//      steps {
//        sh 'npm install'
//      }
//    }
//    stage('Stage release') {
//      steps {
//        sh """
//            git config --global user.email "maximapr1@gmail.com"
//            git config --global user.name "Max"
//           npm run release
//           git status
//           git push --follow-tags origin HEAD
//        """
//      }
//    }
  }
}
