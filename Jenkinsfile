pipeline {
  agent any
  stages {
    stage('Fetch from github') {
      parallel {
        stage('git config-server') {
          steps {
            git(url: 'http://nhattm2@bitbucket.digital.vn/scm/cds/config-server.git', branch: 'dev', credentialsId: 'bitbucket_nhattm2')
          }
        }
        stage('git ci-config') {
          steps {
            git(url: 'http://nhattm2@bitbucket.digital.vn/scm/cds/ci-config.git', branch: 'master', credentialsId: 'bitbucket_nhattm2')
          }
        }
        stage('git ci-db-migration-script') {
          steps {
            git(url: 'http://nhattm2@bitbucket.digital.vn/scm/cds/ci-db-migration-script.git', branch: 'master', credentialsId: 'bitbucket_nhattm2')
          }
        }
        stage('git ci-deployment') {
          steps {
            git(url: 'http://nhattm2@bitbucket.digital.vn/scm/cds/ci-deployment.git', branch: 'master', credentialsId: 'bitbucket_nhattm2')
          }
        }
        stage('ci-jenkins') {
          steps {
            git(url: 'http://nhattm2@bitbucket.digital.vn/scm/cds/ci-jenkins.git', branch: 'master', credentialsId: 'bitbucket_nhattm2')
          }
        }
      }
    }
    stage('Maven Build') {
      steps {
        sh 'echo "Done"'
        dir(path: 'config-server') {
          sh 'echo `pwd`'
        }

      }
    }
  }
}