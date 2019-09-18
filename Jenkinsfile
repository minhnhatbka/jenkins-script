pipeline {
  agent any
  stages {
    stage('Git') {
      steps {
        git(url: 'https://github.com/minhnhatbka/hello.git', branch: 'dev', credentialsId: 'minhnhatbka')
      }
    }
  }
}