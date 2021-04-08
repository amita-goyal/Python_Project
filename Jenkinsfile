pipeline {
  agent any
  stages {
    stage('GIT') {
      steps {
        build 'Python_GIT'
      }
    }

    stage('Web Tests') {
      parallel {
        stage('Web Tests') {
          steps {
            build 'Python_WEB_TESTS'
          }
        }

        stage('') {
          steps {
            build 'Python_API_TESTS'
          }
        }

      }
    }

    stage('API Tests') {
      steps {
        build 'Python_API_TESTS'
      }
    }

    stage('Mobile Tests') {
      steps {
        build 'Python_MOBILE_TESTS'
      }
    }

    stage('Generate Report') {
      steps {
        build 'Python_REPORT_GENERATION'
      }
    }

  }
}