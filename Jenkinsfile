pipeline {
  agent any
  options {
        timeout(time: 1, unit: 'HOURS') 
    }    
  stages {
     
                  stage('CleanWorkspace') {
            steps {
                cleanWs()
            }
        }
                                
                                
                stage("Code Checkout"){
            steps {
                script {
                                                                
                    sh "git clone https://github.com/ankusharma1988/demo.git"
                           
                }
            }
        }      
                                
                                
                                
    
  
  }

}
