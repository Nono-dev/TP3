pipeline {
	agent {
		docker {
			image 'node:6-alpine'
		}
	}

	stages {
	   stage('Build') {
	       steps {
	           sh 'npm install'
	       }
		steps {
		   sh 'npm test'
		}
	   }
	   
	}
}
