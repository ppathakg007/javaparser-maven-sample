pipeline{
	agent any
			stages {
				stage ("code Checkout")
						{
						steps {
						sh env.WORKSPACE = pwd()
						sh echo "$env.WORKSPACE" >> /tmp/log
           					sh "rm ${env.WORKSPACE}/* -fr"
						sh 'git clone https://github.com/ppathakg007/javaparser-maven-sample.git'
						}
						}
					
				stage ("build")
						{
							steps{
							sh 'mvn clean'
							}
						}
				stage (" build Done")
					{
						steps{
							sh ' mvn compile'
						}	
					}
					}
			
		}
