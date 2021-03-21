pipeline {
  agent any
  stages {
    stage('GIT') {
      steps {
        build 'Python_GIT'
      }
    }

    stage('Web Tests') {
      steps {
        build 'Python_WEB_TESTS'
      }
    }

    stage('Rest Tests') {
      steps {
        build 'Python_REST_TESTS'
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