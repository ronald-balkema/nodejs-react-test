pipeline {
    agent {
        docker {
            image 'node:14-alpine'            
        }
    }
	environment {
        CI = 'true'
    }
    stages {
		stage('Wait') {
			steps {
				script {	
					input message: 'Need some input', parameters: [string(defaultValue: '', description: '', name: 'Give me a value')]
				}
			}
		}
        stage('Build') { 
            steps {
				sh 'df'
				sh 'ping -c 3 www.google.com'
				sh 'npm install'		
            }
        }
		
    }
}