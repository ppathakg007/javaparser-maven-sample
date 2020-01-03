pipeline{

tools {
 maven " Maven 3.5.4"
 }

Agen label: ""
stages{
	stage("build"){
	sh 'mvn clean install -Dmaven.test.failure.ignore=true'
	}
}



}
