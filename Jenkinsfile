pipeline{
	agent any
	environment {
		MAVEN_HOME="/opt/apache-maven"
	}
			stages {
								
				stage ("Compile")
						{
							steps{
								sh '${MAVEN_HOME}/bin/mvn clean'
								sh '${MAVEN_HOME}/bin/mvn compile'
							}
						}
				stage (" Test")
					{
						steps{
							sh '${MAVEN_HOME}/bin/mvn test'
						}	
					}
					
				stage (" Package")
					{
						steps{
							sh '${MAVEN_HOME}/bin/mvn package'
						}	
					}
				stage (" verify")
					{
						steps{
							sh '${MAVEN_HOME}/bin/mvn verify'
						}	
					}
				stage (" install")
					{
						steps{
							sh '${MAVEN_HOME}/bin/mvn -X install'
						}	
					}
				stage (" deploy")
					{
						steps{
							sh '${MAVEN_HOME}/bin/mvn deploy'
						}	
					}
					}
}
			
		
