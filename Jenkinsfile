pipeline {
    agent {
        docker {
            image 'node:14-alpine'     
			args '--network host -p 3000:3000'			
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
				sh 'npm install'		
            }
        }
		
    }
}