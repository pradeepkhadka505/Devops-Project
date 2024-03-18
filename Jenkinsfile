

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

        stage ('push-image-at-d-hub'){
	     steps {
	         sh 'sudo docker image tag phptest pradeepkhadka505/php-test:v1'
		 sh 'sudo docker login -u="pradeepkhadka505" -p="Pradeep@khadka@505" && sudo docker phptest pradeepkhadka505/php-test:v1'
		 sh 'echo "image push to docker hub" '
		 }
	}

    }
}

