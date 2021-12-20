pipeline {
  agent any
  options {
        timeout(time: 1, unit: 'HOURS') 
    }    
  
         
                      
   stage("Code Checkout"){
            steps {
                script {
                                                                
                    sh "git clone https://github.com/ankusharma1988/demo.git"
                           
                }
            }
        }  
  
    stage("Build Step"){
            steps {
                script {
                                                                
                    sh "cd $workspace"; sh "cp -rp $workspace/demo/* $workspace";
                    sh "ls -lhrt ";
                    sh "mvn -version  ";
                    sh "mvn clean install"
                   
                    
                }
            }
        }
                                
                                
                                

        
   }
}
