

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
	    sh 'cd Devops-Project/php && sudo docker build -t phptest .'
	    sh 'sudo docker images'
	  }
	}
	stage('push file into Docker hun'){
	steps{
	     echo 'push docker file'
          }
	}
    }
}

