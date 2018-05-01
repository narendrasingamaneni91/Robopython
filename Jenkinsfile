pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/narendrasingamaneni91/Robopython.git', branch: 'master', credentialsId: 'narendrasingamaneni91@gmail.com')
      }
    }
    stage('build') {
      steps {
        echo 'build'
      }
    }
  }
}