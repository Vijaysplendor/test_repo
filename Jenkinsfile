pipeline {
    agent any
	stages {
	   stage ('compiled stage') {
	      steps {
	      withMaven(maven: 'MAVEN_HOME') {
		  sh 'mvn clean compile'
		     }
		  }
	   }
	   stage ('Testing stage') {
	      steps {
	      withMaven(maven: 'MAVEN_HOME') {
		  sh 'mvn test'
		     }
		  }
	   }
	   stage ('Deployment stage') {
	      steps {
	      withMaven(maven: 'MAVEN_HOME') {
		  sh 'mvn deploy'
		     }
		  }
	   }
	}
}