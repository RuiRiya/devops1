pipeline {
  agent any
  stages {
    stage('unitTest') {
      steps {
        echo 'test'
        sh '''pwd
touch pqr
ls'''
      }
    }

    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh 'whoami'
          }
        }

        stage('sonarcubetest') {
          steps {
            sleep 5
            sh 'hostname -i'
          }
        }

      }
    }

    stage('prod') {
      steps {
        echo 'final step'
      }
    }

  }
}