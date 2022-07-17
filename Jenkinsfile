pipeline {
    agent any
	
	 environment{
	 
	  M2_HOME="/opt/maven3/bin"
      PATH = "$M2_HOME:$PATH"
    } 



    stages {
       /* stage('GIT Checkout') {
            steps {
                git credentialsId: 'GITHUBcre', url: 'https://github.com/jmahendra25/DevopsProject2.git'
            }
        }*/
		
		
		stage('Maven Build') {
            steps {
               echo env.PATH
               sh "mvn clean package"
            }
            
        }
		
		stage('Deploy') {
            steps {
           sshagent(['githubpwd']) {

                 sh """
				 scp -o StrictHostKeyChecking=no /var/lib/jenkins/workspace/JenkinsProject2/target/*.war ec2-user@3.7.252.136
					"""

            }
            }
            
        }
		
    }
	
	
        

}
