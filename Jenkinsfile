pipeline {
  agent {
    label 'mac-mini'
  }

  stages {
      stage('INSTALL DEPENDENCIES') {
        steps {
          sh 'yarn'
        }
      }

      stage('BUILD FOR DEV') {

        when {
          expression{ GIT_BRANCH == 'origin/develop' } 
        }

        steps {
          sh 'yarn build:apk'
        }
      }
  }
}
