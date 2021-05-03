pipeline {
      
      agent any 
      
      stages {
      
      stage ("pull from git for sonar") {
        
                steps {
                  git url "https://github.com/madhu-dharmapuri/ansible_3.git"

                }
          }
     
      
      
      stage ("Sonar test analysis") {
             echo 'Sonar Test the file'
                steps { 
                      withSonarQubeEnv('sonarqube') {
                              sh "mvn sonar:sonar \
                                    -Dsonar.projectKey=sonarqube-1 \
                                    -Dsonar.host.url=http://192.168.122.1:9000 \
                                    -Dsonar.login=4b192d4f3f528bedac3352df66dace38bfafd1ad"
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
