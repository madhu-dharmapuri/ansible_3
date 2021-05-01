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
                        def test = 2 + 2 > 6 ? 'Wrong' : 'Right'
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
