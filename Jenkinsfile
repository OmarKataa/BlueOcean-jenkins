
def value = true
pipeline {
  agent any

  // environment{

  //   // credential=credentials('id')
  //   // value = true
  // }
  parameters{

    choice(name: 'value',choices: ['true'] , description: '')
  }
  stages {
     
    stage('Build') {
      when{

          expression{
            params.value == 'true'
          }
        }
      steps {

        script{

          gv = load "fn.groovy"
        }
        echo 'build success'
        script{

          gv.fn()
        }
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

      input{

          message "enter name"
          ok "Done"
          parameters{
            choice(name: "name", choices:['omar','ahmad'],description:"")
          }
        }
      steps {

        script{
        echo "name ${name}"
        }// input(message: 'are you sure?', ok: 'yes')
        echo 'success code'
      }
    }

  }
}