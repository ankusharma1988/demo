pipeline {
  agent any
  environment {
    APPSYSID = 'a0e34d791be401101c7a415de54bcb06'
    BRANCH = "${BRANCH_NAME}"
    CREDENTIALS = 'servicenow'
    DEVENV = 'https://hclnowintelligence.service-now.com/'
    TESTENV = 'https://hcltechdemosls4.service-now.com/'
    PRODENV = 'https://prodinstance.service-now.com/'
    TESTSUITEID = 'bf8c266d732333005ce769972bf6a777'
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
                                
       stage('Test') {
         steps {
        snInstallApp(credentialsId: "${CREDENTIALS}", url: "${TESTENV}", appSysId: "${APPSYSID}")
        
         }
     }                
                                
    
  
  }

}
