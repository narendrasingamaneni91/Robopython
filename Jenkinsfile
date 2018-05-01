pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/narendrasingamaneni91/Robopython.git', branch: 'master', credentialsId: 'narendrasingamaneni91')
      }
    }
    stage('build') {
      steps {
        echo 'build'
      }
    }
  }
}