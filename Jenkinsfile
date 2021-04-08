pipeline {
  agent any
  stages {
    stage('GIT') {
      steps {
        build 'Python_GIT'
      }
    }

    stage('Different Tests') {
      parallel {
        stage('Web Tests') {
          steps {
            build 'Python_WEB_TESTS'
          }
        }

        stage('API tests') {
          steps {
            build 'Python_API_TESTS'
          }
        }

        stage('Mobile Tests') {
          steps {
            build 'Python_MOBILE_TESTS'
          }
        }

        stage('Generate Allure Report') {
          steps {
            build 'Python_REPORT_GENERATION'
          }
        }

      }
    }

    stage('Generate Report') {
      steps {
        build 'Python_REPORT_GENERATION'
      }
    }

  }
}