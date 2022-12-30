pipeline {
  agent any
	tools {
		maven 'maven 3.8.6'
	}
  stages {
    stage ('BUILD MAVEN') {
      steps {
	      checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Vinay-RR/Test_Java.git']])
        sh 'mvn clean install'
      }  
    }  
      stage ('BUILD DOCKER IMAGE') {
	   steps {
		   script {
			   sh 'docker build -t devops-integration .'
      }  
      }  
    }  
  } 
}
