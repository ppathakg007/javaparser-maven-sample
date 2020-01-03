pipeline{
	environment{
		M2_HOME="/opt/apache-maven"
	}
tools {
 maven " Maven 3.5.4"
 }

Agen label: ""
stages{
	Stage("code checout"){
		sh 'git clone git@github.com:ppathakg007/javaparser-maven-sample.git'
	}
	stage( " Clean repo"){
		sh '$M2_HOME\bin\mvn clean'
	}
	stage("build"){
	sh '$M2_HOME\bin\mvn compile'
	}
}



}
