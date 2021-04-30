pipeline {
      
      agent any 
      
      stages {
      
      stage ("build") {
          steps {
          echo 'Build the file'
          }
     
      }
      
      stage ("test") {
          steps {
          echo 'Test the file'
                script {
                def testing = 2 + 3 > 6 ? 'No' : 'Yes' 
                      echo testin
                }
          }
      
      }
      
      
      stage ("deploy") {
          steps {
          echo 'Deploy the file'
          }
      
      }
      
      
      }
      
}
