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
	}
	stages {
	   stage ('Testing stage') {
	      steps {
	      withMaven(maven: 'MAVEN_HOME') {
		  sh 'mvn test'
		     }
		  }
	   }
	}
	stages {
	   stage ('Deployment stage') {
	      steps {
	      withMaven(maven: 'MAVEN_HOME') {
		  sh 'mvn deploy'
		     }
		  }
	   }
	}
}