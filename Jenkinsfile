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
	   }
	    stage('Test') {
		steps {
		   sh 'npm test'
		}
	    }
            stage('Deploiement ansible') {
	        steps {
		    ansiblePlaybook (
		      colorized: true, 
		      become: true,
		      inventory: 'inventaire.ini'
		      playbook: 'playbook.yml'
		    )
		} 
	    }
	}
}
