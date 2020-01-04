pipeline{
	agent any
			stages {
				stage ("code Checkout")
						{
						git clone https://github.com/ppathakg007/javaparser-maven-sample.git
						}
					
				stage ("build")
						{
							steps{
							echo "test pipeline"
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
