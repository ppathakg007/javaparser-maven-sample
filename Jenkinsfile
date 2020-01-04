pipeline{
	agent any
			stages {
				stage ("code Checkout")
						{
						steps {
						sh 'git clone https://github.com/ppathakg007/javaparser-maven-sample.git'
						}
						}
					
				stage ("build")
						{
							steps{
							sh 'mvn compile'
							}
						}
				stage (" build Done")
					{
						steps{
							echo "CICD DONE"
						}	
					}
					}
			
		}
