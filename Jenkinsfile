pipeline {
  agent any

  options {
    buildDiscarder(logRotator(numToKeepStr:'2', artifactNumToKeepStr: '1'))
  }

  stages {
    stage('build') {
      agent {
        label 'apache'
      }
      steps {
        sh 'ant -f build.xml -v'
      }
    }
  }
  post {
    always {
      archive 'dist/*.jar'
     }
  }
}
