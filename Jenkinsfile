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
     
     stages {
    stage('Build') {
      steps {
        snApplyChanges(appSysId: "${APPSYSID}", branchName: "${BRANCH}", url: "${DEVENV}", credentialsId: "${CREDENTIALS}")
        snPublishApp(credentialsId: "${CREDENTIALS}", url: "${DEVENV}", appSysId: "${APPSYSID}",
          isAppCustomization: true, obtainVersionAutomatically: true, incrementBy: 2)
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
