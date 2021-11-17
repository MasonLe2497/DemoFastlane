pipeline {
  agent {
    label 'master'
  }

  stages {
      stage('INSTALL DEPENDENCIES') {
        steps {
          sh 'npm install'
        }
      }

      stage('BUILD FOR DEV') {

        when {
          expression{ GIT_BRANCH == 'origin/develop' } 
        }

        steps {
          sh 'npm run build:apk'
        }
      }
  }
}
