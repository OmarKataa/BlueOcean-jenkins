pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'build success'
      }
    }

    stage('Test Stage') {
      parallel {
        stage('Test Stage') {
          steps {
            echo 'test1'
          }
        }

        stage('Teststage2') {
          steps {
            echo 'test2'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'success deploy'
      }
    }

  }
}