

pipeline {
    agent any

    stages {
        stage('Automation') {
            steps {
                echo 'Project Automations '
            }
        }
        stage('directory-view'){
            steps{
                
                sh 'ls -ltr'
                sh 'pwd'
            }
        }
	
        stage('docker-build) {
	     steps {
	     echo 'Docker build'
	     }
	 }
    }
}

