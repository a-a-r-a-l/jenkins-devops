pipeline {
	agent any
	stages {
	
	environment {
	    dockerHome =tool 'myDocker'
	    mavenHome = tool 'myMaven'
	    PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	    stage('Build') {
		steps{
		   sh 'mvn --version'
		   sh 'docker version'
		   echo "Build"
		   echo "PATH - ${PATH}"
		   echo "BUILD_NUMBER - ${BUILD_NUMBER}"
		   echo "BUILD_ID - ${BUILD_ID}"
		   echo "JOB_NAME - ${JOB_NAME}"
		   echo "BUILD_TAG - ${BUILD_TAG}"
		   echo "BUILD_URL - ${BUILD_URL}"
		}
	    }
	
	    stage('Test') {
		steps{
		   echo "Test"
		}
	    }
	
	    stage('Integration Test') {
		steps{
		   echo "Integration Test"
		}
	    }
	}
	post{
	    always {
	        echo "I always run"
	    }
	    success {
	        echo "I run when you are successful"
	    }
	    failure { 
	        echo "I run when you fail"
	    }
	}
	
}

