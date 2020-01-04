pipeline{
	agent any
	environment {
		MAVEN_HOME="/opt/apache-maven"
	}
			stages {
				//stage ("code Checkout")
				//		{
				//		steps {
				//		sh env.WORKSPACE = pwd()
           			//		sh "rm ${env.WORKSPACE}/* -fr"
				//		sh 'git clone https://github.com/ppathakg007/javaparser-maven-sample.git'
				//		}
				//		}
					
				stage ("build")
						{
							steps{
								sh '${MAVEN_HOME}/bin/mvn clean'
							}
						}
				stage (" build Done")
					{
						steps{
							sh '${MAVEN_HOME}/bin/mvn compile'
						}	
					}
					}
			
		}
