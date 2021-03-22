pipeline {
    agent {
        docker {
            image 'node:6-alpine' 
            args '-p 3000:3000' 
        }
    }
	environment {
        CI = 'true'
    }
    stages {
        stage('Build') { 
            steps {
				sh 'df'
				sh 'ping -c 3 www.google.com'
				
				input message: "Approve build?" submitter: "admin_group"
                sh 'npm install' 
            }
        }
    }
}