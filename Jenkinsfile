pipeline {
    node { label "linux-node" }
 parameters {
  //  gitParameter branchFilter: 'origin/(.*)', defaultValue: 'master', name: 'BRANCH', type: 'PT_BRANCH'
    // parameters { string(name: 'NODE', defaultValue: 'some_node', description: '') }
   gitParameter branchFilter: 'origin/(.*)', defaultValue: 'master', name: 'BRANCH', type: 'PT_BRANCH',string(name: 'NODE', defaultValue: 'master', description: '')

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
