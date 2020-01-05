pipeline{
	agent any
	environment {
		MAVEN_HOME="/opt/apache-maven"
	}
			stages {
								
				stage ("Compile")
						{
							steps{
							//	input message: 'Please input to proceed', ok: 'GO Ahead'
								sh '${MAVEN_HOME}/bin/mvn -X clean'
								sh '${MAVEN_HOME}/bin/mvn -X compile'
							}
						}
				stage (" Test")
					{
						steps{
							sh '${MAVEN_HOME}/bin/mvn -X test'
						}	
					}
					
				stage (" Package")
					{
						steps{
							sh '${MAVEN_HOME}/bin/mvn -X package'
						}	
					}
				stage (" verify")
					{
						steps{
							sh '${MAVEN_HOME}/bin/mvn -X verify'
						}	
					}
				stage (" install")
					{
						steps{
							sh '${MAVEN_HOME}/bin/mvn -X install'
						}	
					}
				//stage (" deploy")
					//{
						//steps{
							//sh '${MAVEN_HOME}/bin/mvn -X deploy'
					//	}	
					//}
					}
			postBuild
					{
						always
							{
								archive "target/**/*"
								junit 'target/surefire-reports/*.xml'
							}
					}
			notifications
						{
							success
									{
									mail(to:ppathakg007@gmail.com",subject:"success:${currentBuild.fullDisplayName}",body: "Yay,We Passwd.")
									}
							failure
									{
									mail(to:ppathakg007@gmail.com",subject:"success:${currentBuild.fullDisplayName}",body: "Huh,We failed.")
									}
							unstable
									{
									mail(to:ppathakg007@gmail.com",subject:"success:${currentBuild.fullDisplayName}",uff: "Yay,We are Unstable.")
									}
						}
}
