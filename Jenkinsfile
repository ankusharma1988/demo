pipeline {
  agent any
   
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
                                
       stage('Test') {
         steps {
        snInstallApp(credentialsId: "${CREDENTIALS}", url: "${TESTENV}", appSysId: "${APPSYSID}")
        
         }
     }  
    
  }
                                
    
  
  }

}
