pipeline {
  agent any
  stages {
    stage('GIT') {
      steps {
        build 'Git'
      }
    }

    stage('Python Tests') {
      steps {
        build 'Python_WebTests'
      }
    }

  }
}