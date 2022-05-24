pipeline {
  agent any

  environment{

    // credential=credentials('id')
    value=true
  }
  stages {
    stage('Build') {
      steps {
        echo 'build success'
        // echo "${credential}"
        
        when{

          expression{
            value
          }
        }
       echo "omar"
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
            echo 'test2'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        // input(message: 'are you sure?', ok: 'yes')
        echo 'success deploy'
    
      
       
      //  sh "credentials ${credential}"
      
      }
    }

    stage('code') {
      steps {
        // input(message: 'are you sure?', ok: 'yes')
        echo 'success code'
      }
    }

  }
}