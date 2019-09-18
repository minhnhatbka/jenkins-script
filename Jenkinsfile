pipeline {
  agent any
  stages {
    stage('Git') {
      steps {
        git(url: 'http://nhattm2@bitbucket.digital.vn/scm/cds/config-server.git', branch: 'dev', credentialsId: 'bitbucket_nhattm2')
      }
    }
  }
}