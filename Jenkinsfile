pipeline {
  agent any

  tools {nodejs "node"}

  stages {
    stage('Example') {
      steps {
        sh 'npm --version'
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
//        """
//      }
//    }
//    stage('Stage push') {
//      steps {
//        sh """
//           npm run release:tags
//        """
//      }
//    }
  }
}
