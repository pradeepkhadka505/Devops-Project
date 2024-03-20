

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
        
         stage ('push-image-at-d-hub'){
             steps {
                 sh 'sudo docker image tag phptest pradeepkhadka505/phptest:v1'
                 sh 'sudo docker login -u="pradeepkhadka505@gmail.com" -p="Pradeep@Khadka@505" && sudo docker push pradeepkhadka505/phptest:v1'
		 sh 'sudo image pushed to docker hub'
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

