

pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('git-clone'){
            steps{
                sh 'git clone https://github.com/pradeepkhadka505/Devops-Project.git'
                sh 'ls -ltr'
                sh 'pwd'
            }
        }
    }
}

