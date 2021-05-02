pipeline {
      
      agent any 
      
      stages {
      
      stage ("pull from git for sonar") {
        
                steps {
                  git url "https://github.com/madhu-dharmapuri/ansible_3.git"

                }
          }
     
      }
      
      stage ("Sonar test analysis") {
             echo 'Sonar Test the file'
                steps { 
                      withSonarQubeEnv('sonarqube') {
                              sh "./gradlew sonarqube"
                      }
                }
      
      }
            
      
      stage ("Sonar qualitygate test") {
          steps {
          echo 'SOnar qualitygate test'
                 waitForQualityGate abortpipeline: true
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
