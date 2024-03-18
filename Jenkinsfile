

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
		sh 'ls -ltr Devops-Project/'
            }
        }
	
        stage('docker-build') {
	   steps {
	          sh 'cd Devops-Project/php && sudo docker build -t phptest .'
	          sh 'sudo docker images'
	     }
	 }

	stage('mysql-build') {
	     steps {
		  sh 'cd Devops-Project/mysql && sudo docker build -t mysqldb .'
		  sh 'sudo docker image ls'

            }
        }

    }
}

