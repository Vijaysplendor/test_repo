pipeline {
    agent any
	stages {
	   stage ('compiled stage') {
	      withMaven(maven: 'MAVEN_HOME') {
		  sh 'mvn clean compile'
		  }
	   }
	}
	stages {
	   stage ('Testing stage') {
	      withMaven(maven: 'MAVEN_HOME') {
		  sh 'mvn test'
		  }
	   }
	}
	stages {
	   stage ('Deployment stage') {
	      withMaven(maven: 'MAVEN_HOME') {
		  sh 'mvn deploy'
		  }
	   }
	}
}