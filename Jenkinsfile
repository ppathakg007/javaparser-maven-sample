pipeline{

tools {
 maven " Maven 3.5.4"
 }

Agen label: ""
stages{
	Stage("code checout"){
		sh 'git clone git@github.com:ppathakg007/javaparser-maven-sample.git'
	}
	stage( " Clean repo"){
		sh 'mvn clean'
	}
	stage("build"){
	sh 'mvn compile'
	}
}



}
