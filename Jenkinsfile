pipeline {
    agent { label "linux-node" }
 parameters {
 properties([parameters([string(defaultValue: 'main', description: 'please enter branch name you want to build!!', name: 'branch_name')])])

  }
    stages {
	    stage('Checkout') {           	
            steps {
             checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/sathishreddy844/java-tomcat-maven-docker.git']]])
		
            }
        }
	    stage('Build and Package') {           	
            steps {
                    
		 script{
		    sh """
		    ls
		   #  mvn clean package
		   echo  "MAster"
		   ls -la               
		   """
		 }
	 
            }
        }
       
    }  
}
