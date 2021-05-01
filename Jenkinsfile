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
                      echo test
                }
                
          }
      
      }
      
      
      stage ("deploy") {
          steps {
          echo 'Deploy the file'
                script {
                        def deploy = 2 + 2 > 6 ? 'Wrong' : 'Right'
                        echo deploy
                }
          }
      
      }
      
      
      }
      
}
