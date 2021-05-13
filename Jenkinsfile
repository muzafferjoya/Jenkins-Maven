pipeline {
  agent {
    docker {
      image 'maven'
      args '-v /root/.m2:/root/.m2'
    }

  }
  stages {
    stage('Buzz Build') {
      steps {
        sh './jenkins/build.sh'
      }
    }

    stage('Buzz Test') {
      steps {
        sh './jenkins/test-all.sh'
      }
    }

  }
}
