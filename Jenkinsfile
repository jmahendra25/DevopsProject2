pipeline {
    agent any
	
	 environment{
	 
	  M2_HOME="/opt/maven386/bin"
      PATH = "$M2_HOME:$PATH"
    } 



    stages {
        stage('GIT Checkout') {
            steps {
                git credentialsId: 'GITHUBcre', url: 'https://github.com/jmahendra25/DevopsProject2.git'
            }
        }
		
		
		stage('Maven Build') {
            steps {
               echo env.PATH
               sh "mvn clean package"
            }
            
        }
    }
	
	
        

}
