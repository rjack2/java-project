pipeline {
  agent any

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
