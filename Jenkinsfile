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
        input(message: 'are you sure?', ok: 'yes')
        echo 'success deploy'
      }
    }

    stage('notify') {
      steps {
        echo 'success'
      }
    }

  }
}