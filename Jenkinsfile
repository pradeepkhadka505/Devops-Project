

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
	stage('docker-build'){
	steps{
	    sh 'cd Devops-Project/php && sudo docker build -t phptst .'
	    sh 'sudo docker image ls'
	    
	  }
	}
    }
}

