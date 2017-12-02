pipeline {
  agent none

  environment {
    MAJOR_VERSION = 1
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
}
