pipeline {
      
      agent any 
      
      stages {
      
      stage ("pull from git for sonar") {
          steps {
          echo 'pull the git'
                  script {
                        def build = 2 + 2 < 6 ? 'Wrong build' : 'Right build done well '
                      echo build
                      
                  }
                steps {
                  git url "https://github.com/madhu-dharmapuri/ansible_3.git"

                }
          }
     
      }
      
      stage ("Sonar test analysis") {
          steps {
          echo 'Sonar Test the file'
                script {
                        def test = 2 + 2 > 6 ? 'Wrong test' : 'Right test done'
                      echo test
                }
                steps { 
                      withSonarQubeEnv('sonarqube') {
                              sh "./gradlew sonarqube"
                      }
                }
                
          }
      
      }
            
      
      stage ("Sonar qualitygate test") {
          steps {
          echo 'SOnar qualitygate test'
                script {
                        def test = 2 + 2 > 6 ? 'Wrong test' : 'Right test  done'
                      echo test
                }
                steps {
                        waitForQualityGate abortpipeline: true
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
