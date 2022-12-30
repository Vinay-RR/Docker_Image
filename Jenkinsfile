pipeline {
	agent {
  label 'maven_project'
}
      stages {
    stage ('BUILD MAVEN') {
      steps {
	      checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Vinay-RR/Devops-October-2022/tree/main/applications/maven_app/src/main/java/com/harsha/calculator']])
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
