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
					}
}
			
		
