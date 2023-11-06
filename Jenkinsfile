pipeline {
	agent any 
	parameters {
		triggers {
  pollSCM '*/5 * * * *'
}
	}
	stages {
	    stage('Checkout') {
	        steps {
			checkout scm			       
		      }}
		stage('Build') {
	           steps {
			  sh '/home/dev/Documents/devopssoftware/apache-maven-3.9.5/bin/mvn install'
	                 }}
		stage('Deployment'){
		   steps {
		sh 'cp target/star1.war /home/dev/Documents/devopssoftware/apache-tomcat-9.0.82/webapps'
			}}	
}}
