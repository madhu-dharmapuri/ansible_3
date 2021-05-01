pipeline {
      
      agent any 
      
      stages {
      
      stage ("build") {
          steps {
          echo 'Build the file'
                  script {
                        def build = 2 + 2 < 6 ? 'Wrong build' : 'Right build done well'
                      echo build
                  }
          }
     
      }
      
      stage ("test") {
          steps {
          echo 'Test the file'
                script {
                        def test = 2 + 2 > 6 ? 'Wrong test' : 'Right test done'
                      echo test
                }
                
          }
      
      }
      
      
      stage ("deploy") {
          steps {
          echo 'Deploy the file'
                script {
                        def deploy = 2 + 2 > 6 ? 'Wrong deploy' : 'Right deploy done'
                        echo deploy
                }
          }
      
      }
      
      
      }
      
}
