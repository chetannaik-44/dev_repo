// Declarative pipeline
pipeline {
    agent any

    stages {

        stage ('Git Checkout') {
            steps {
                git branch: 'main', credentialsId: 'github', url: 'https://github.com/chetannaik-44/dev_repo.git'
            }
        }
        
        stage ('Build Docker Image') {
            steps {
                sh 'docker-compose build '       
            }
        }
    }
}