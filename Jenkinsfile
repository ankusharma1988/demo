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
                                                                
                    sh "https://github.com/ankusharma1988/demo.git"
                           
                }
            }
        }      
                                
                                
                                
    stage("Build Step"){
            steps {
                script {
                                                                
                    sh "cd $workspace"; sh "cp -rp $workspace/Demo /* $workspace";
                    sh "ls -lhrt ";
                    sh "mvn -version  ";
                    sh "mvn clean install"
                   
                    
                }
            }
        }
        
        }

}
