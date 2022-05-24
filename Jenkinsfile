pipeline {
  agent any

  environment{

    // credential=credentials('id')
    value=true
  }
  stages {
     
    stage('Build') {
      when{

          expression{
            ${value} == true
          }
        }
      steps {
        echo 'build success'
        // echo "${credential}"
        
       
       
      }
    }

    stage('Test Stage') {
      parallel {
        stage('Test Stage') {
          steps {
            echo 'test1'
            echo "${value}"
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