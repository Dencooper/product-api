pipeline{  

	agent any 
	
	stages{ 
		stage('Build') { 
			steps { 
				bat 'mvn deploy' 
			} 
		} 
		
		stage('Test') { 
			steps { 
				bat 'mvn test' 
			} 
		} 
		
		stage('Deployment') { 
			steps { 
				bat 'mvn clean deploy -Pdev -DmuleDeploy -s settings.xml' 
			}  
		} 
	} 
}	