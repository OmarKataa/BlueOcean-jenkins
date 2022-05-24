pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'build success'
        echo '$BRANCH_NAME'
        sh 'echo $BRANCH_FILE'
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

    stage('code') {
      steps {
        input(message: 'are you sure?', ok: 'yes')
        echo 'success code'
      }
    }

  }
}